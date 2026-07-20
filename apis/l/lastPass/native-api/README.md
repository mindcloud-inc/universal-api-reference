# LastPass: Native API Reference

A consolidated summary of LastPass's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://support.lastpass.com/help/use-the-lastpass-enterprise-api-postman-collection
- **API base URL:** `https://lastpass.com`

## Authentication

### Provisioning API Credentials

Authenticate to the LastPass Enterprise provisioning API with your CID account number and provisioning hash.

### Credentials

- **CID:** `cid` · required · LastPass Enterprise CID account number.
- **Provisioning Hash:** `provhash` · required · LastPass Enterprise provisioning hash.

[Official authentication documentation](https://support.lastpass.com/help/use-the-lastpass-enterprise-api-postman-collection)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create User](actions/create-user.md) | `POST /enterpriseapi.php` | [docs](https://support.lastpass.com/help/use-the-lastpass-enterprise-api-postman-collection) |
| [Delete User](actions/delete-user.md) | `POST /enterpriseapi.php` | [docs](https://support.lastpass.com/help/use-the-lastpass-enterprise-api-postman-collection) |
| [Disable Multifactor](actions/disable-multifactor.md) | `POST /enterpriseapi.php` | [docs](https://support.lastpass.com/help/lastpass-provisioning-api) |
| [Disable User](actions/disable-user.md) | `POST /enterpriseapi.php` | [docs](https://support.lastpass.com/help/lastpass-provisioning-api) |
| [Enable User](actions/enable-user.md) | `POST /enterpriseapi.php` | [docs](https://support.lastpass.com/help/lastpass-provisioning-api) |
| [Get Detailed Shared Folder Data](actions/get-detailed-shared-folder-data.md) | `POST /enterpriseapi.php` | [docs](https://support.lastpass.com/help/use-the-lastpass-enterprise-api-postman-collection) |
| [Get Reporting Data](actions/get-reporting-data.md) | `POST /enterpriseapi.php` | [docs](https://support.lastpass.com/help/lastpass-provisioning-api) |
| [Get Shared Folder Data](actions/get-shared-folder-data.md) | `POST /enterpriseapi.php` | [docs](https://support.lastpass.com/help/use-the-lastpass-enterprise-api-postman-collection) |
| [Get User Data](actions/get-user-data.md) | `POST /enterpriseapi.php` | [docs](https://support.lastpass.com/help/use-the-lastpass-enterprise-api-postman-collection) |
| [Reinvite User](actions/reinvite-user.md) | `POST /enterpriseapi.php` | [docs](https://support.lastpass.com/help/lastpass-provisioning-api) |
| [Require Master Password Change](actions/require-master-password-change.md) | `POST /enterpriseapi.php` | [docs](https://support.lastpass.com/help/lastpass-provisioning-api) |
| [Send Password Reset Email](actions/send-password-reset-email.md) | `POST /enterpriseapi.php` | [docs](https://support.lastpass.com/help/lastpass-provisioning-api) |
| [Update User Email](actions/update-user-email.md) | `POST /enterpriseapi.php` | [docs](https://support.lastpass.com/help/lastpass-provisioning-api) |
