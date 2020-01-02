# Country_gii
Tutorial on using Yii2 with Gii using the Country database from the previous tutorial

If you need to create the Country database and table the sql is here:

*Create a Database:*
```
CREATE SCHEMA IF NOT EXISTS `country_gii`;
USE `country_gii`;
```

*Database Table:*
```
 CREATE TABLE `country` (
  `code` CHAR(2) NOT NULL PRIMARY KEY,
  `name` CHAR(52) NOT NULL,
  `population` INT(11) NOT NULL DEFAULT '0'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

INSERT INTO `country` VALUES ('AU','Australia',24016400);
INSERT INTO `country` VALUES ('BR','Brazil',205722000);
INSERT INTO `country` VALUES ('CA','Canada',35985751);
INSERT INTO `country` VALUES ('CN','China',1375210000);
INSERT INTO `country` VALUES ('DE','Germany',81459000);
INSERT INTO `country` VALUES ('FR','France',64513242);
INSERT INTO `country` VALUES ('GB','United Kingdom',65097000);
INSERT INTO `country` VALUES ('IN','India',1285400000);
INSERT INTO `country` VALUES ('RU','Russia',146519759);
INSERT INTO `country` VALUES ('US','United States',322976000);
```

Now we'll create a project:

Using Terminal, create a "country_gii" directory in the "tutorial" directory and download Yii2 Basic to it. *Change the Paths as appropriate*:
```
cd ~/www/tutorial/
composer create-project --prefer-dist yiisoft/yii2-app-basic country_gii
```

Create a GIT repo on github.com called: Country_gii

Now initialise git on your computer (change [YOUR_GITHUB_NAME] as required):
```
cd ~/www/tutorial/country_gii
git init
git commit -m "first commit"
git remote add origin git@github.com:[YOUR_GITHUB_NAME]/Country_gii.git
git push -u origin master
```

Start Netbeans and create a new PHP project with existing sources using the country_gii directory

