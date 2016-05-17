# zurmo-db-compatibility
Updated mysql database connection related scripts

## Description
In PHP 7, `mysql` function isn't supported. So, we need to change some Zurmo CRM scripts which still implements `mysql` functions into `mysqli`.
The scripts is started from the Zurmo CRM installation phase. Installation process will be fail if we use old scripts in PHP 7 environment.
The scripts which need to be changed are as following.  

1. app\protected\commands\tests\unit\DatabaseCommandTest.php 
2. app\protected\core\tests\unit\DatabaseCompatibilityUtilTest.php 
3. app\protected\core\utils\DatabaseCompatibilityUtil.php 

Replace all scripts with the new one.