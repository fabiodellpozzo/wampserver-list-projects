# wampserver-list-projects
Alteração para exibição link de projetos locais index.php do wamp.

Wampserver
Apache 2.4 - MySQL 5 & 8 - MariaDB 10 - PHP 5, 7 & 8  3.3.0 - 64bit

Alteração entre as linhas 530 - 560 

		$projectContents .= ($wampConf['LinksOnProjectsHomePage'] == 'off') ? "     //<---  alterado de on para off 
