# Codeigniter user module

Complete module for user management

## Getting Started

Used CodeIgniter Version 3.1.9 + PHP 7.2.4 + MySQL

### Prerequisites

PHP 5.6+, MySQL

Table users
```sql
CREATE TABLE `users` (
  `id` int(11) NOT NULL,
  `session_id` varchar(50) COLLATE utf8_unicode_ci NOT NULL,
  `nivel` int(11) NOT NULL,
  `name` varchar(255) COLLATE utf8_unicode_ci NOT NULL,
  `email` varchar(100) COLLATE utf8_unicode_ci NOT NULL,
  `password` varchar(50) COLLATE utf8_unicode_ci NOT NULL,
  `active` int(11) NOT NULL DEFAULT '1',
  `created` timestamp NULL DEFAULT CURRENT_TIMESTAMP,
  `updated` timestamp NULL DEFAULT NULL
) ENGINE=MyISAM DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;    

ALTER TABLE `users`
  ADD PRIMARY KEY (`id`);    

ALTER TABLE `users`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;
```
Table ci_sessions
```sql
CREATE TABLE `ci_sessions` (
  `id` varchar(128) COLLATE utf8_unicode_ci NOT NULL,
  `ip_address` varchar(45) COLLATE utf8_unicode_ci NOT NULL,
  `timestamp` int(10) UNSIGNED NOT NULL DEFAULT '0',
  `data` blob NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;

ALTER TABLE `ci_sessions`
  ADD KEY `ci_sessions_timestamp` (`timestamp`);
```
## Built With

* [CodeIgniter 3](https://codeigniter.com/) - The web framework used
* [Modular Extensions - HMVC](https://bitbucket.org/wiredesignz/codeigniter-modular-extensions-hmvc) - Dependency Management

## Authors

* **LeoFeitosa** - *Initial work* - [LeoFeitosa](https://github.com/LeoFeitosa)

## License

This project is licensed under the MIT License - see the [MIT license](LICENSE) file for details
