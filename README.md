# yorkspace-customizations
YUL custom styling, lang files and other configurations.

Steps
1) Download Dspace 6 source
2) Copy yorkspace-customizations/config/* to [dspace-source]/dspace/config
3) Copy yorkspace-customizations/i18n to /[dspace-source]/dspace/modules/xmlui-mirage2/src/main/webapp/
4) Copy yorkspace-customizations/themes to /[dspace-source]/dspace/modules/xmlui-mirage2/src/main/webapp/
5) cd to [dspace-source]/dspace
6) mvn clean
7) mvn package -Dmirage2.on=true
8) cd to [dspace-source]/target/dspace-installer/
9) sudo -utomcat8 ant update 
10) sudo /path/to/tomcat8 restart (e.g. /etc/init.d/tomcat8)

