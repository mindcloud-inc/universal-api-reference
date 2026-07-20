# <img src="https://images.mindcloud.co/apps/icons/verifalia_1774637924192.png" alt="Verifalia logo" width="28" height="28"> Verifalia: Universal API

Email verification and mailing-list cleaning platform with credits, validation jobs, and team-management APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/verifalia/latest
- **Category:** Marketing
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://verifalia.com
- **Vendor API docs:** https://verifalia.com/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits Balance](actions/get-credits-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/get-credits-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Client Certificate

| Action | Method | Description |
| --- | --- | --- |
| [Delete User Certificate](actions/delete-user-certificate.md) | DELETE | Deletes a user certificate from Verifalia. |
| [List User Certificates](actions/list-user-certificates.md) | GET | Retrieves user certificates from Verifalia. |
| [Upload User Certificate](actions/upload-user-certificate.md) | POST | Uploads a user certificate to Verifalia. |

### Contact Method

| Action | Method | Description |
| --- | --- | --- |
| [Activate Contact Method](actions/activate-contact-method.md) | PUT | Activates a contact method in Verifalia. |
| [Create Contact Method](actions/create-contact-method.md) | POST | Creates a new contact method in Verifalia. |
| [Delete Contact Method](actions/delete-contact-method.md) | DELETE | Deletes an existing contact method from Verifalia. |
| [Get Contact Method](actions/get-contact-method.md) | GET | Retrieves a contact method from Verifalia. |
| [List Contact Methods](actions/list-contact-methods.md) | GET | Retrieves contact methods from Verifalia. |
| [Update Contact Method](actions/update-contact-method.md) | PUT | Updates an existing contact method in Verifalia. |

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits Balance](actions/get-credits-balance.md) | GET | Retrieves the current credits balance from Verifalia. |

### Daily Credit Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Credit Usage](actions/get-daily-credit-usage.md) | GET | Retrieves daily credit usage from Verifalia. |

### Email Validation Job

| Action | Method | Description |
| --- | --- | --- |
| [Delete Validation Job](actions/delete-validation-job.md) | DELETE | Deletes an email validation job from Verifalia. |
| [Get Validation Job](actions/get-validation-job.md) | GET | Retrieves an email validation job from Verifalia. |
| [Import Validation File](actions/import-validation-file.md) | POST | Creates a new email validation job from a file in Verifalia. |
| [List Validation Jobs](actions/list-validation-jobs.md) | GET | Retrieves email validation jobs from Verifalia. |
| [Submit Validation Job](actions/submit-validation-job.md) | POST | Creates a new email validation job in Verifalia. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Verifalia. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Verifalia. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Verifalia. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Verifalia. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Verifalia. |

### Validation Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Validation Job Entry](actions/get-validation-job-entry.md) | GET | Retrieves an entry from an email validation job in Verifalia. |
| [List Validation Job Entries](actions/list-validation-job-entries.md) | GET | Retrieves entries from an email validation job in Verifalia. |

### Validation Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Validation Job Entries](actions/export-validation-job-entries.md) | GET | Retrieves exported email validation entries from Verifalia. |

### Validation Overview

| Action | Method | Description |
| --- | --- | --- |
| [Get Validation Job Overview](actions/get-validation-job-overview.md) | GET | Retrieves an email validation job overview from Verifalia. |

