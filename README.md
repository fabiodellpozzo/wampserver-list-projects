# wampserver-list-projects
Alteração para exibição link de projetos locais na home do wampp.

Wampserver
Apache 2.4 - MySQL 5 & 8 - MariaDB 10 - PHP 5, 7 & 8

3.3.0 - 64bit

Alteração na linha 561 

// Project recovery

$list_projects = array();

$handle = opendir(".");

while (false !== ($file = readdir($handle))) {
	if (is_dir($file) && !in_array($file, $projectsListIgnore))
		$list_projects[] = $file;
		
}

closedir($handle);

$projectContents = '';

if (count($list_projects) > 0) {
	if ($wampConf['LinksOnProjectsHomePage'] == 'on') {
		$projectContents .= "<p class='projectsdir'>http://localhost/project/</p>\n";
	}
	foreach ($list_projects as $file) {
	
		$projectContents .= ($wampConf['LinksOnProjectsHomePage'] == 'off') ? "     //<---  alterado de on para off 
