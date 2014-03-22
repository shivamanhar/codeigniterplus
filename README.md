Codeigniterplus (The Ultimate Codeigniter Enhancements)
=====================================

Codeigniterplus is an super light-weight codeigniter based extension with various other third party libraries. This will help developers
to have a kick-ass start along their way to web application development.

(View Live Demo: http://demo.codesamplez.com/codeigniterplus/)

(And introductory post to codeigniterplus: http://codesamplez.com/project/codeigniter-bundle )

Release Note For v2.0.0
----------------------
- Update CodeIgniter to latest version(v2.1.4)
- Updated Hybridauth to version.(THere was some updates, but didn't see any new release tag, confused :s)
- Update Smarty to new version.
- Added Composer Support.(Currently only doctrine is installed from composer, but you can install anything else as well. 
See documentation for details: https://getcomposer.org/doc/00-intro.md) 

Release Note For v1.1.1
----------------------
- Updated libraries to their latest versions.(see latest included version besides the library listing)

Release Note For v1.1.0
----------------------
- Added 'Twitter Bootstrap' framework. (Special Thanks to Bogdan Comarniceanu, https://www.facebook.com/bcomarniceanu)
- Fix few small issues/validation errors.
	
Libraries used:
------------------
- PHP libraries
	* DX_Auth (https://github.com/EllisLab/CodeIgniter/wiki/DX-Auth)
	* Hybridauth (social login library: http://hybridauth.sourceforge.net/, Included version 2.1.2)
	* Doctrine (http://www.doctrine-project.org/, Included version 2.3.3)
	* Smarty (http://www.smarty.net/ , Included version 3.1.13)
	* HMVC (https://bitbucket.org/wiredesignz/codeigniter-modular-extensions-hmvc) 
        * Composer Dependency Manager.(https://getcomposer.org/)

- Styles
	* Twitter Bootstrap(http://twitter.github.com/bootstrap/ , Included version 2.3.1) [ Replaced The Previous 'Blue Print CSS' (http://www.blueprintcss.org/) From version 1.1.0 ]

- Javascript Libraries
       * Jquery (http://jquery.com/ , Included version 2.0.0)
       * Jquery UI (http://jqueryui.com/ , Included version 1.10.2)
       * Google map API (https://developers.google.com/maps/)
       * Google Map API Wrapper(http://hpneo.github.io/gmaps/, Included version 0.3.3 )
       * Steal.js from JavascriptMVC (http://javascriptmvc.com/docs.html#!stealjs)
       * jQuery Validate Plugin(https://github.com/jzaefferer/jquery-validation , Included version 1.11.1)
       * jQuery Form Plugin(https://github.com/malsup/form/ , Included version 3.9)
       * Twitter Bootstrap(http://twitter.github.com/bootstrap/ , Included version 2.3.1)

Features:
----------
- A number of popular open source libraries to boost codeigniter development with your existing knowledge on them.(See above)
- Organized directory structure for view files/stylesheets and javascript files.
- Loading view template automatically based on the name of Controller and function.(Inspired from Asp.NET MVC architecture)
- Load javascripts libraries in asynchronous request, helping your application get the maximum performance.
- Load stylesheet files/javascript files automatically if exist for a specific page. No external include/import required.
- detect domain name automatically and add to the page title. Of course option also available for add page title/meta key and 
meta descriptions as well.
- custom javascript "on load" function for your page, where you can initialize page specific tasks.
- Use ORM(doctrine) for database layer.
- User template engine(smarty) for view layer.
- Automatic client validation binding for forms all over the application(using jquery validate plugin). Also, custom enhanced style 
  applied to validation error message placeholder.
- Being ahead to the new era of PHP along with Composer, the dependency manage for PHP. You can install virtually anything(which have provided 
composer support) with it and use without any trouble.

Technical Requirement
---------------------
- PHP version 5.3.x
- Mysql version 5.x+ Database Engine(Should work with other db as well which doctrine support. But I haven't tested yet)
- Composer(to install and use third party libraries through it, which is highly recommended).

Installation
----------
- Crate a new project with your chosen name. 
- Paste all file from CodeIgniterPlus to your project directory.
- Run "composer update" command to get doctrine dependency installed.
- Change 'RewriteBase' on '.htaccess' file as per your your chosen name. If using root level domain, just remove it and keep as 'RewriteBase /'. 
- Create a database with your given database name in config/database.php file.
- Now edit config/database.php file; Here change the database server, database name, user name and password as per your database server.
- Make sure the following directories exists(create if not) and do have write permission by the application(easy to have them with '777' mode):
    * {root}/application/cache
    * {root}/application/logs
    * {root}/application/models/proxies
- Run http://{domain_path}/home/db_schema for create database tables from the doctrine entities, automatically.
  (Note :Every time when you update your entity file in models/entity directory just Run the above url for update existing schema.)
- run the application, register with username 'admin'. This will cause to create default two roles 'admin' and user automatically and will 
  make user 'admin' in 'admin' role. From this on, whenever a registration happens, all will be assigned default 'user' role.
  (Note: If you wish to change this functionality please do so on 'application/libraries/DX_Auth.php', starting at line 930.)

If you want to avoid composer:
To avoid using it, you just have to download and add the doctrine library files inside 'third_party' manually by yourself. also edit the
libraries/doctrine.php, enable line 37 and then change the path in line 39 to "APPPATH.'third_party'". also, remove the 'MY_Composer' 
from autoload.php library section. You should be fine now.


Basic functionality
-------------------
- You will get default functionality and directory/file structure built in for three different section.
- Front end, or publicly viewable pages.
- User end, when registered members can login and have their accessible functionality.
- Admin end, to perform administration functionality. You have your freedom to add as much as you want :).

Your Contribution
-------------------

I will love to get your contribution on this project. If you are interested, please feel free to add issues/bugs as you found from the 
project(https://github.com/ranacseruet/codeigniterplus/issues?state=open). Also, if you have a new idea which can improve its usability
or functionality, please add them there too. If you are interested to work and contribute the code, add yourself as assignee
(or let me know if you need my help), fork the repo, make changes, commit and make an pull request.

