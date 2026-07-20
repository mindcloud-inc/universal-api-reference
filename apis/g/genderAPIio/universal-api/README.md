# <img src="https://images.mindcloud.co/apps/icons/apps_1781896357020.png" alt="GenderAPI.io logo" width="28" height="28"> GenderAPI.io: Universal API

Infer gender and validate phone numbers from names, emails, and usernames

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/genderAPIio/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.genderapi.io/
- **Vendor API docs:** https://www.genderapi.io/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Remaining Credits](actions/get-remaining-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/get-remaining-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Remaining Credits](actions/get-remaining-credits.md) | GET | Retrieves remaining API credits from GenderAPI.io. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Gender by Email](actions/get-gender-by-email.md) | GET | Retrieves gender details from GenderAPI.io by email address. |
| [Get Gender by Email Batch](actions/get-gender-by-email-batch.md) | GET | Retrieves gender details from GenderAPI.io for multiple email addresses. |
| [Get Gender by Email (GET)](actions/get-gender-by-email-get.md) | GET | Retrieves gender details from GenderAPI.io by email address. |
| [Get Gender by Name](actions/get-gender-by-name.md) | GET | Retrieves gender details from GenderAPI.io by name. |
| [Get Gender by Name Batch](actions/get-gender-by-name-batch.md) | GET | Retrieves gender details from GenderAPI.io for multiple names. |
| [Get Gender by Name (GET)](actions/get-gender-by-name-get.md) | GET | Retrieves gender details from GenderAPI.io by name. |
| [Get Gender by Username](actions/get-gender-by-username.md) | GET | Retrieves gender details from GenderAPI.io by username. |
| [Get Gender by Username Batch](actions/get-gender-by-username-batch.md) | GET | Retrieves gender details from GenderAPI.io for multiple usernames. |
| [Get Gender by Username (GET)](actions/get-gender-by-username-get.md) | GET | Retrieves gender details from GenderAPI.io by username. |
| [Validate Phone Number](actions/validate-phone-number.md) | GET | Retrieves phone validation details from GenderAPI.io. |
| [Validate Phone Number (GET)](actions/validate-phone-number-get.md) | GET | Retrieves phone validation details from GenderAPI.io. |

