PHP for login
=================================

A very simple php script for login via mysql.

How to setup script
---
Create database "test" and create table "users" :
```
CREATE TABLE `users` (
  `ID` mediumint(9) NOT NULL,
  `email` varchar(50) DEFAULT NULL,
  `password` varchar(50) DEFAULT NULL,
  `fullname` varchar(50) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

INSERT INTO `users` (`ID`, `email`, `password`, `fullname`) VALUES
(1, 'admin@admin.com', '21232f297a57a5a743894a0e4a801fc3', 'Administrator');

ALTER TABLE `users` ADD PRIMARY KEY (`ID`);
ALTER TABLE `users` MODIFY `ID` mediumint(9) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=7;
```

Setup the db-config.php file
---
```
$db_address  = ""; // "127.0.0.1";
$db_name     = ""; // "test";
$db_username = ""; // "root";
$db_password = ""; // "";

$site_security_key = ""; //try to set strong key
```

Default user/pass is admin/admin.


License
---
```
Copyright 2016 Mohammad Yaghobi

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```