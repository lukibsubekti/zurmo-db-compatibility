# zurmo-db-compatibility
Updated mysql database connection related scripts

## Description
In PHP 7, `mysql` function isn't supported. So, we need to change several Zurmo CRM scripts which still implement `mysql` functions into `mysqli`. The scripts are started from the Zurmo CRM installation phase. The installation process will fail if we use old scripts in PHP 7 environment. The scripts which need to be replaced after the installation process are as follows.

1. `app\protected\commands\tests\unit\DatabaseCommandTest.php`
2. `app\protected\core\tests\unit\DatabaseCompatibilityUtilTest.php`
3. `app\protected\core\utils\DatabaseCompatibilityUtil.php`

Replace all scripts with new ones.
