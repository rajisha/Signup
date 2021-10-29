# Signup 

Added Signup form and validations

### Installation

#### New Pre-Requisites
1. PHP `v7.2` or above.
2. MySQL `(5.1+)` via the MySQLi driver.
3. PHP Extensions required

   3.1 `intl`  

   3.2 `mbstring`

   3.3 `json`

   3.4 `mysqlnd`

   3.5 `libcurl`

4. XAMPP Control panel v3.2.4
5. For run this api using `Postman` desktop agent
`http://localhost/codeigniter/signup` -For leading signup form
`
6. Add this db query for checking 
```
CREATE TABLE `users` (
  `id` int(11) NOT NULL,
  `name` varchar(150) DEFAULT NULL,
  `email` varchar(200) DEFAULT NULL,
  `phone` varchar(50) DEFAULT NULL,
  `username` varchar(150) DEFAULT NULL,
  `password` varchar(150) DEFAULT NULL,
  `role` enum('0','1') NOT NULL DEFAULT '0' COMMENT '0=>Customer,1=>shop'
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

ALTER TABLE `users`
  ADD PRIMARY KEY (`id`);

ALTER TABLE `users`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;

```

## New Framework CI v4.1.3 Setup

1. Copy contents from `env` file to `.env` and make the following changes
    1.1 Change the `ENVIRONMENT` variable  `# CI_ENVIRONMENT = production` to 

        1.1.1 `CI_ENVIRONMENT = development` if development

    1.2 Change the `APP` variable  `#app.baseURL = ''` to 

        1.2.1 `app.baseURL = 'http://localhost/{localfolder}/'` if local.

    1.3 Change the `App` variable  `#app.CSPEnabled = true` to 

        1.3.1 `app.CSPEnabled = true`

    1.4 Change the `DATABASE` settings after removing the `#` from the below variables

        `database.default.hostname = database host name`

        `database.default.database = database name`

        `database.default.username = database username`

        `database.default.password = database password`

        `database.default.DBDriver = MySQLi`

2. Copy the contents of `htaccess.txt` file from the public/ folder to the file `.htaccess` in the root folder.

3. After step 1 and step 2, still some issues found then check the `writable` folder and provide full permissions for it.
