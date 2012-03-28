# MIBS

This repository is a colleciton of SNMP mibs. Sometimes you only need a few, but
the fact of the matter is - disk space is cheap. 

If we can collect these all in one place once and for all, we will have saved
untold amounts of pain and suffering for the remainder of time.

## "Help! My mib is missing!"

Do one of the following;

 1) Send me a link to the mibs you want to include
 2) Fork this repostiory, add your mibs and send me a pull request

## Using the MIBS

### Net-SNMP (Must die but I digress)

Copy the mib files you care about into your snmp mib path. To find that out, run

    $ net-snmp-config --default-mibdirs

Then copy your files in

    $ cp ALL_THE_MIBS /opt/local/share/snmp/mibs

If you want to use the mibs *all* of the time, then you also have to include the
mibs when you load tools. If you load all of the mibs all of the time, then that
can incur an unfair performance penalty. The trade-off is up to you.

Find the name of your MIB (you usually have to crack it open to find it) then
include it by adding the following line (for example) into your snmp.conf file

    mibs +TCP-MIB


