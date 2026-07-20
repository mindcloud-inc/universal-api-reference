# <img src="https://images.mindcloud.co/apps/icons/a194bf2f-a678-4609-b5d3-d4f0f469059b_1780948216899.png" alt="AnyDB logo" width="28" height="28"> AnyDB: Universal API

Manage AnyDB teams, databases, records, shares, and webhooks through AnyDB's external integration API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/anyDB/latest
- **Category:** IT Operations / Database
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.anydb.io/
- **Vendor API docs:** https://www.anydb.com/support/integrations/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate API Key And Email](actions/validate-api-key-and-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/validate-api-key-and-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Complete Upload](actions/complete-upload.md) | PUT | Completes an attachment upload in AnyDB. |
| [Get Download URL](actions/get-download-url.md) | GET | Retrieves a download URL for an AnyDB attachment. |
| [Get Upload URL](actions/get-upload-url.md) | GET | Retrieves a direct upload URL for AnyDB attachments. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [List Databases For Team](actions/list-databases-for-team.md) | GET | Retrieves databases for a team in AnyDB. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a new record in AnyDB. |
| [Duplicate Record](actions/duplicate-record.md) | POST | Creates a duplicate record in AnyDB. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from AnyDB by ID. |
| [List Records](actions/list-records.md) | GET | Retrieves records from AnyDB with optional filters and pagination. |
| [Remove Record From Parents](actions/remove-record-from-parents.md) | DELETE | Removes a record from parent records in AnyDB. |
| [Search Records](actions/search-records.md) | GET | Finds records in AnyDB by search text. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in AnyDB. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Validate API Key And Email](actions/validate-api-key-and-email.md) | GET | Validates API key and email in AnyDB. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams for the authenticated AnyDB user. |

