# yorkspace-customizations
YUL custom styling, lang files and other configurations.
### About the Files

| File      | Info  | 
|:------------------- |:---------------|
| **config/local.cfg.tempate** | One config file to rule them all! Dspace has many new config files and can get messing keeping track of them all. No longer! Copy this file and override as needed / change-me fields and that is all! |
| **config/news-xmlui.xml** | Text that displays on landing page. Better to edit lang file in modules i18n directory unless there is more content that needs to be added (add new content to lang file as well)|
| **modules/xmlui-mirage2/.../i18n/\***   | English and French lang files override |
| **modules/xmlui-mirage2/.../themes/Mirage2/\***  | xsl templates, images, styling files |


###Steps
1. Download [Dspace 6 source](https://github.com/DSpace/DSpace)
2. `cd [dspace-source]`
3. `git clone https://github.com/yorkulibraries/yorkspace-customizations.git ./dspace` (This will copy repo files to [dspace-source]/dspace folder where they belong without messing any other files. See .gitignore
4. `cd [dspace-source]/dspace/config`
5. `mv local.cfg.template local.cfg`
6. edit `local.cfg` and look for string `"change-me"` to update relavent fields (mail settings are defaulted to YorkU)
7. Edit further language or theme changes (see file info above)
8. `cd to [dspace-source]/dspace`
9. `mvn clean`
10. `mvn package -Dmirage2.on=true `
11. `cd to [dspace-source]/target/dspace-installer/`
12. `chmod -R a+rwx .`
13. `sudo -utomcat8 ant update `
14. `sudo /path/to/tomcat8 restart` (e.g. /etc/init.d/tomcat8) 

