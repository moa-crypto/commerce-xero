# Changelog

## 3.0.0 - 2024-10-22

### Changed
- Now requires Craft 5.0+.
- Now requires Craft Commerce 5.0+.

## 2.0.1 - 2024-12-31

### Fixed
- Fix organisation validation occurring before being connected.
- Fix lack of error handling for organisations that have lost their connection.
- Fix lack of organisation name when saved, but not connected to a tenant.
- Improve instruction text for new organisations.

## 2.0.0 - 2024-10-22
> {note} The plugin’s package name has changed to `verbb/xero`. Xero will need be updated to 2.0 from a terminal, by running `composer require verbb/xero && composer remove thejoshsmith/commerce-xero`.

### Added
- Added Organisations view.
- Added the ability to create multiple organisations, each pushing data to.
- Add the ability to set invoice status and line item type.

### Changed
- Migration to `verbb/xero`.
- Migration to `verbb/auth` for OAuth handling.
- Now requires Craft 4.0+.
- Now requires Craft Commerce 4.0+.

## 1.0.4.1 - 2021-03-09

### Fixed
- Fixed an issue with a migration that wasn't using Yii's table prefix syntax.

## 1.0.4 - 2021-03-09
### Fixed
- Fixed an issue with a DB where clause that wasn't using Yii's table prefix syntax.

## 1.0.3 - 2021-02-28

### Fixed
- Fixed an issue with PostgreSQL where boolean values were cast as integers and therefore failed model validation
- Re-enabled db transaction when saving connections

## 1.0.2 - 2021-02-28

### Changed
- Custom CP triggers are now supported
- Added a plugin description and settings shortcut

### Fixed
- Fixed an issue where Yii's dependency injection was creating an object without the required token parameter
- Fixed a minor issue where side bar meta instructions were showing pre Craft version 3.5.17
- Fixed an issue where the callback shown was hard coded to my dev callback URL 🤦
- Fixed an issue where certain DB columns weren't nullable

## 1.0.1 - 2021-02-15

### Fixed
- Fixed an issue where cp nav item wasn't showing sub menu
- Fixed a minor issue where a successful connection saved notice was always shown, even if it wasn't the case
- Improved robustness of selecting the current organisation with a db transaction

## 1.0.0 - 2021-02-13

### Changed
- Plugin has been shifted to a new repository `thejoshsmith/commerce-xero`
- Improved model validation

### Fixed
- Restored the "Send to Xero" functionality from completed orders
- Fixed a bug where switching organisations would overwrite the Xero connection ID with the plugin's connection ID

## 1.0.0-beta.2 - 2021-02-13

### Changed
- Users can now select from a list of organisations
- Improved multi-tenant support
- Users can now disconnect organisations programatically

### Fixed
- Fixed a bug where the current connection wasn't returning the right organisation

## 1.0.0-beta.1 - 2021-02-12

### Changed
- Added support for Xero OAuth 2.0
- Plugin now has a CP nav item
- Account code mappings and settings can be changed in production mode
- Refactored code base

## 0.9.3 - 2019-10-05

### Changed
- order items sent to Xero now use Crafts prodsuct description, which if isn't set defaults to title.
- fixed an issue where active carts weren't viewable when plugin was enabled.
- example xero.php config file include for multi environment setups.

## 0.9.2 - 2019-08-21

### Changed
- ca-bundle.crt is now required in settings, documentation has been updated. A ca-bundle file can easily be downloaded from github or firefox and then put in the same folder as your other cert files.

## 0.9.1 - 2019-08-01

### Fixed
- Fixed an issue where items where passing through an incorrect total

## 0.9.0 - 2019-07-20

### Added
- Initial BETA release
- Added ability to connect to Xero
- Added ability to configure Chart of Accounts
- Added ability autmatically send invoices to Xero
- Added ability to manually send invoices to Xero