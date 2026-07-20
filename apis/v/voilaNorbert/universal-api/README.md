# <img src="https://images.mindcloud.co/apps/icons/voila-norbert_1774899797606.png" alt="VoilaNorbert logo" width="28" height="28"> VoilaNorbert: Universal API

Find work emails and enrich prospect contacts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/voilaNorbert/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.voilanorbert.com/
- **Vendor API docs:** https://api.voilanorbert.com/2018-01-08/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves current account details from VoilaNorbert. |

### Bulk File

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk File](actions/get-bulk-file.md) | GET | Retrieves a bulk file status from VoilaNorbert. |
| [List Bulk Files](actions/list-bulk-files.md) | GET | Retrieves bulk files from VoilaNorbert in chronological order. |
| [Submit Bulk File](actions/submit-bulk-file.md) | POST | Submits a bulk email search file to VoilaNorbert. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a single contact from VoilaNorbert. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from VoilaNorbert. |
| [Search By Domain](actions/search-by-domain.md) | POST | Finds contacts in VoilaNorbert by domain or company name. |
| [Search By Name](actions/search-by-name.md) | POST | Finds a contact in VoilaNorbert by full name and domain. |

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Credits](actions/get-organization-credits.md) | GET | Retrieves current organization credits from VoilaNorbert. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Pause Bulk File](actions/pause-bulk-file.md) | PUT | Pauses an active bulk file in VoilaNorbert. |
| [Remove Bulk File](actions/remove-bulk-file.md) | DELETE | Deletes a bulk file from VoilaNorbert. |
| [Resume Bulk File](actions/resume-bulk-file.md) | PUT | Resumes a paused bulk file in VoilaNorbert. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in VoilaNorbert. |
| [Get List](actions/get-list.md) | GET | Retrieves one list from VoilaNorbert. |
| [List Lists](actions/list-lists.md) | GET | Retrieves your contact lists from VoilaNorbert. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in VoilaNorbert. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves current organization details from VoilaNorbert. |

