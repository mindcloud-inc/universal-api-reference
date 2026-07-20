# Verifalia: Native API Reference

A consolidated summary of Verifalia's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://verifalia.com/developers
- **API base URL:** `https://api-1.verifalia.com/v2.7`

## Authentication

### Basic Auth

Connect with your Verifalia username and password. Verifalia recommends using a dedicated API user instead of the root account.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://verifalia.com/developers/authentication)

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Contact Method](actions/activate-contact-method.md) | `PUT /users/{user-id}/contact-methods/{contact-method-id}/activation` | [docs](https://verifalia.com/developers/users/contact-methods) |
| [Create Contact Method](actions/create-contact-method.md) | `POST /users/{user-id}/contact-methods` | [docs](https://verifalia.com/developers/users/contact-methods) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://verifalia.com/developers/users) |
| [Delete Contact Method](actions/delete-contact-method.md) | `DELETE /users/{user-id}/contact-methods/{contact-method-id}` | [docs](https://verifalia.com/developers/users/contact-methods) |
| [Delete User](actions/delete-user.md) | `DELETE /users/{user-id}` | [docs](https://verifalia.com/developers/users) |
| [Delete User Certificate](actions/delete-user-certificate.md) | `DELETE /users/{user-id}/certificates/{certificate-id}` | [docs](https://verifalia.com/developers/users/client-certificates) |
| [Delete Validation Job](actions/delete-validation-job.md) | `DELETE /email-validations/{id}` | [docs](https://verifalia.com/developers/email-verifications/deleting-jobs) |
| [Export Validation Job Entries](actions/export-validation-job-entries.md) | `GET /email-validations/{id}/entries` | [docs](https://verifalia.com/developers/email-verifications/retrieving-jobs) |
| [Get Contact Method](actions/get-contact-method.md) | `GET /users/{user-id}/contact-methods/{contact-method-id}` | [docs](https://verifalia.com/developers/users/contact-methods) |
| [Get Credits Balance](actions/get-credits-balance.md) | `GET /credits/balance` | [docs](https://verifalia.com/developers/credits) |
| [Get Daily Credit Usage](actions/get-daily-credit-usage.md) | `GET /credits/daily-usage` | [docs](https://verifalia.com/developers/credits) |
| [Get User](actions/get-user.md) | `GET /users/{user-id}` | [docs](https://verifalia.com/developers/users) |
| [Get Validation Job](actions/get-validation-job.md) | `GET /email-validations/{id}` | [docs](https://verifalia.com/developers/email-verifications/retrieving-jobs) |
| [Get Validation Job Entry](actions/get-validation-job-entry.md) | `GET /email-validations/{id}/entries/{index}` | [docs](https://verifalia.com/developers/email-verifications/retrieving-jobs) |
| [Get Validation Job Overview](actions/get-validation-job-overview.md) | `GET /email-validations/{id}/overview` | [docs](https://verifalia.com/developers/email-verifications/retrieving-jobs) |
| [Import Validation File](actions/import-validation-file.md) | `POST /email-validations` | [docs](https://verifalia.com/developers/email-verifications/creating-jobs) |
| [List Contact Methods](actions/list-contact-methods.md) | `GET /users/{user-id}/contact-methods` | [docs](https://verifalia.com/developers/users/contact-methods) |
| [List User Certificates](actions/list-user-certificates.md) | `GET /users/{user-id}/certificates` | [docs](https://verifalia.com/developers/users/client-certificates) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://verifalia.com/developers/users) |
| [List Validation Job Entries](actions/list-validation-job-entries.md) | `GET /email-validations/{id}/entries` | [docs](https://verifalia.com/developers/email-verifications/retrieving-jobs) |
| [List Validation Jobs](actions/list-validation-jobs.md) | `GET /email-validations` | [docs](https://verifalia.com/developers/email-verifications/listing-jobs) |
| [Submit Validation Job](actions/submit-validation-job.md) | `POST /email-validations` | [docs](https://verifalia.com/developers/email-verifications/creating-jobs) |
| [Update Contact Method](actions/update-contact-method.md) | `PATCH /users/{user-id}/contact-methods/{contact-method-id}` | [docs](https://verifalia.com/developers/users/contact-methods) |
| [Update User](actions/update-user.md) | `PATCH /users/{user-id}` | [docs](https://verifalia.com/developers/users) |
| [Upload User Certificate](actions/upload-user-certificate.md) | `POST /users/{user-id}/certificates` | [docs](https://verifalia.com/developers/users/client-certificates) |
