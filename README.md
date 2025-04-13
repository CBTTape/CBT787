# CBT787
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. GitHub repos will be deleted and created during this period...

```
//***FILE 787 is from Karl-Heinz Doppelfeld and contains an         *   FILE 787
//*           online File Transfer Utility for sending data to a    *   FILE 787
//*           generated list of remote hosts.  The list of remote   *   FILE 787
//*           hosts will be generated from ClonePlex System         *   FILE 787
//*           table BWSOSDAT.  The target name can include          *   FILE 787
//*           system symbols like &SYSNAME, &SYSUQ, &SYSCLONE       *   FILE 787
//*           and &SYSRZ.                                           *   FILE 787
//*                                                                 *   FILE 787
//*       External Subroutines: $FTPSMAC - edit macro to change     *   FILE 787
//*                                        system symbols in        *   FILE 787
//*                                        target dataset names     *   FILE 787
//*                                                                 *   FILE 787
//*       email:  Karl-Heinz.Doppelfeld@Sparkassen-Informatik.de    *   FILE 787
//*                                                                 *   FILE 787
//*                    - - - Description: - - -                     *   FILE 787
//*                                                                 *   FILE 787
//*    Online Filetransfer Utility for sending data to a            *   FILE 787
//*    generated list of remote Hosts.  The list of remote Hosts    *   FILE 787
//*    will be generated from System name table.  The target        *   FILE 787
//*    name can include system symbols defined in the system        *   FILE 787
//*    name table.                                                  *   FILE 787
//*                                                                 *   FILE 787
//*    FIRST SOME EXPLANATION WHAT IS THE IDEA FOR THE UTILITY:     *   FILE 787
//*                                                                 *   FILE 787
//*     We have a multi sysplex environment with min. 4 up to 8     *   FILE 787
//*     systems in each sysplex.  One system is our distribution    *   FILE 787
//*     system from which we are doing most of the work for all     *   FILE 787
//*     systems.  For it we have an table driven ISPF dialog.       *   FILE 787
//*     One table has an entry for system in our complete           *   FILE 787
//*     company.  For each system we have defined some - STATIC     *   FILE 787
//*     - system symbols in this table, like SYSNAME SYSPLEX        *   FILE 787
//*     SYSCLONE etc.                                               *   FILE 787
//*                                                                 *   FILE 787
//*     SO, HOW CAN I SEND OR GET A LITTLE PORTION OF DATA FROM     *   FILE 787
//*     OR TO ALL SYSTEMS? - I know the great utility FTPB from     *   FILE 787
//*     Lionel B. Dyck to do this for a great/greater portion       *   FILE 787
//*     but I want transfer a member of a PDS or a little PS        *   FILE 787
//*     interactively to all, some or one system in our             *   FILE 787
//*     company.                                                    *   FILE 787
//*                                                                 *   FILE 787
//*    ENHANCEMENTS FOR USING IT OUTSIDE OF OUR COMPANY:            *   FILE 787
//*                                                                 *   FILE 787
//*     Build and use an extra SYSTEM NAME table outside of         *   FILE 787
//*     our dialog where you must define all systems in YOUR        *   FILE 787
//*     company.  You can use the utility in ADMIN or USER          *   FILE 787
//*     mode. In ADMIN mode only the user specified as admin        *   FILE 787
//*     (aUserid) can modify the system name table. In USER         *   FILE 787
//*     mode everybody can do it. For it you can set the            *   FILE 787
//*     dataset where the system name table resides to a            *   FILE 787
//*     global dataset or to a user dataset like ISPF profile       *   FILE 787
//*     dataset.  To modify the system name table I check           *   FILE 787
//*     whether the calling user is the ADMIN user and will         *   FILE 787
//*     see a modified panel with an extra command available        *   FILE 787
//*     called 'SETSYST'. If anybody knows the command and he       *   FILE 787
//*     is not the ADMIN user he will be informed by a message      *   FILE 787
//*     that he can not use the command.                            *   FILE 787
//*                                                                 *   FILE 787
//*     On some systems you may have different userids, so I        *   FILE 787
//*     have defined an extra table where any user can store        *   FILE 787
//*     his own remote userids.  This extra table resides in        *   FILE 787
//*     your ISPF profile dataset.                                  *   FILE 787
//*                                                                 *   FILE 787
//*     Because we have a special naming convention I have          *   FILE 787
//*     implemented to special switches for including or            *   FILE 787
//*     excluding from sending or getting the data.  You can        *   FILE 787
//*     adjust the names of the switches to own names.  The         *   FILE 787
//*     names will be shown in the primary panel.                   *   FILE 787
//*                                                                 *   FILE 787
//*    HOW DOES THE UTILITY WORK:                                   *   FILE 787
//*                                                                 *   FILE 787
//*     After you have called the utility the first time a          *   FILE 787
//*     SYSTEM NAME table with one dummy entry will be              *   FILE 787
//*     created.  Please customize the table before further         *   FILE 787
//*     usage.                                                      *   FILE 787
//*                                                                 *   FILE 787
//*     For each entry entry you must specify the following:        *   FILE 787
//*                                                                 *   FILE 787
//*       SYSNAME      - the system name                            *   FILE 787
//*       DNS/Ip-add   - the systems DNS or IP-Add.                 *   FILE 787
//*       act          - switch Y/N; only to active systems         *   FILE 787
//*                      data will be send                          *   FILE 787
//*       prod         - is it a production system or not           *   FILE 787
//*       mstr         - (we have in each sysplex one master        *   FILE 787
//*                      system.)  you can use it in conjunction    *   FILE 787
//*                      with the BOUNDARY switch in the primary    *   FILE 787
//*                      panel to send data only to this master     *   FILE 787
//*                      system or to all systems in the sysplex    *   FILE 787
//*       incl         - send data to this system even you have     *   FILE 787
//*                      set the BOUNDARY to 'X' (only to one       *   FILE 787
//*                      system in a plex)                          *   FILE 787
//*       excl         - do not send data to this system            *   FILE 787
//*       SYSPLEX      - the sysplex name where the system runs     *   FILE 787
//*                                                                 *   FILE 787
//*                                                                 *   FILE 787
//*       Please see member $$NOTE1 for further installation        *   FILE 787
//*       details.                                                  *   FILE 787
//*                                                                 *   FILE 787
```
