concrete5-install-issue
=======================

Concrete5.7.2.1 install issues on clean servers

Following error keeps coming up every single time i try to install Concrete5 FULL INSTALL.

Tested with two clean servers, no change.

It always takes me back to the "install page". No clue what so ever to do with this. Changing language won't do anything.

Problem:

An exception occurred while executing 'INSERT INTO SystemDatabaseMigrations (version) VALUES (?)' with params ["20141113000000"]: SQLSTATE[23000]: Integrity constraint violation: 1062 Duplicate entry '20141113000000' for key 'PRIMARY'.

Trace:
#0 /home/sg2133/public_html/home/concrete5.7.2.1/concrete/vendor/doctrine/dbal/lib/Doctrine/DBAL/Connection.php(702): Doctrine\DBAL\DBALException::driverExceptionDuringQuery(Object(PDOException), 'INSERT INTO Sys...', Array) #1 /home/sg2133/public_html/home/concrete5.7.2.1/concrete/vendor/doctrine/migrations/lib/Doctrine/DBAL/Migrations/Version.php(150): Doctrine\DBAL\Connection->executeQuery('INSERT INTO Sys...', Array) #2 /home/sg2133/public_html/home/concrete5.7.2.1/concrete/src/Package/StartingPointPackage.php(195): Doctrine\DBAL\Migrations\Version->markMigrated() #3 [internal function]: Concrete\Core\Package\StartingPointPackage->install_database() #4 /home/sg2133/public_html/home/concrete5.7.2.1/concrete/controllers/install.php(282): call_user_func(Array) #5 [internal function]: Concrete\Controller\Install->run_routine('elemental_full', 'install_databas...') #6 /home/sg2133/public_html/home/concrete5.7.2.1/concrete/src/Controller/AbstractController.php(156): call_user_func_array(Array, Array) #7 /home/sg2133/public_html/home/concrete5.7.2.1/concrete/src/Routing/ControllerRouteCallback.php(25): Concrete\Core\Controller\AbstractController->runAction('run_routine', Array) #8 /home/sg2133/public_html/home/concrete5.7.2.1/concrete/src/Routing/Router.php(59): Concrete\Core\Routing\ControllerRouteCallback->execute(Object(Concrete\Core\Http\Request), Object(Concrete\Core\Routing\Route), Array) #9 /home/sg2133/public_html/home/concrete5.7.2.1/concrete/src/Support/Facade/Facade.php(116): Concrete\Core\Routing\Router->execute(Object(Concrete\Core\Routing\Route), Array) #10 /home/sg2133/public_html/home/concrete5.7.2.1/concrete/src/Application/Application.php(340): Concrete\Core\Support\Facade\Facade::__callStatic('execute', Array) #11 /home/sg2133/public_html/home/concrete5.7.2.1/concrete/src/Application/Application.php(340): Concrete\Core\Support\Facade\Route::execute(Object(Concrete\Core\Routing\Route), Array) #12 /home/sg2133/public_html/home/concrete5.7.2.1/concrete/bootstrap/start.php(196): Concrete\Core\Application\Application->dispatch(Object(Concrete\Core\Http\Request)) #13 /home/sg2133/public_html/home/concrete5.7.2.1/concrete/dispatcher.php(36): require('/home/sg2133/pu...') #14 /home/sg2133/public_html/home/concrete5.7.2.1/index.php(2): require('/home/sg2133/pu...') #15 {main}
