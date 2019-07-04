**Place images, styles, xsl and _style.scss files in**
``` 
/[dspace-source]/dspace/modules/xmlui-mirage2/src/main/webapp/themes/Mirage2 folder
```

```
cd /[dspace-source]/dspace
mvn clean
mvn package -Dmirage2.on=true
```

OR (to be safe, even after mvn clean)
```
mvn -U clean package -Dmirage2.on=true 
cd [dspace-source]/target/dspace-installer
sudo -utomcat8 ant update
sudo /etc/init.d/tomcat8 restart

```


