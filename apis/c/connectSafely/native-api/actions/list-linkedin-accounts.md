# List connected LinkedIn accounts (lightweight + searchable) with ConnectSafely

Returns a lightweight list of the LinkedIn accounts visible to the caller (their own plus any shared via a workspace). This is a fast, **database-only** endpoint — it does NOT call LinkedIn or fetch premium status — so it is the preferred way to populate account pickers and run searches.

Each item includes `apiSeatAllocated`, indicating whether the caller currently holds an active API seat for that account.

Use the optional `q` query parameter to search. `q` matches (case-insensitive) against firstName, lastName and publicId; if `q` is a 24-character account id it matches that account exactly; and if `q` is a LinkedIn profile URL the public_id slug is extracted and matched against publicId.

**Example requests:**
- `GET /linkedin/accounts` — all visible accounts
- `GET /linkedin/accounts?q=john` — by first/last name or public id
- `GET /linkedin/accounts?q=john-doe-123` — by public id
- `GET /linkedin/accounts?q=60d21b4667d0d8992e610c85` — exact account id
- `GET /linkedin/accounts?q=https://www.linkedin.com/in/john-doe-123/` — by LinkedIn profile URL

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [List connected LinkedIn accounts (lightweight + searchable)](https://connectsafely.ai/docs/api/linkedin-account/get-accounts-list-linkedin-accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Optional search term. Matches firstName / lastName / publicId (case-insensitive), an exact 24-hex account id, or a LinkedIn profile URL (the public_id slug is extracted). |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].id` | `string` | LinkedIn account id (Mongo ObjectId) |
| `[].firstName` | `string` |  |
| `[].lastName` | `string` |  |
| `[].publicId` | `string` | LinkedIn public identifier (the slug after linkedin.com/in/) |
| `[].picture` | `string` | Profile picture URL |
| `[].status` | `string` | Account status (e.g., AVAILABLE, WARMUP, ERROR, UNKNOWN) |
| `[].enabled` | `boolean` |  |
| `[].apiSeatAllocated` | `boolean` | True when the caller holds an active API seat for this account |

### Example response

```json
[
  {
    "id": "60d21b4667d0d8992e610c85",
    "firstName": "John",
    "lastName": "Doe",
    "publicId": "john-doe-123",
    "picture": "https://media.licdn.com/dms/image/v2/D5603...",
    "status": "AVAILABLE",
    "enabled": true,
    "apiSeatAllocated": true
  },
  {
    "id": "60d21b4667d0d8992e610c86",
    "firstName": "Jane",
    "lastName": "Smith",
    "publicId": "jane-smith",
    "picture": null,
    "status": "WARMUP",
    "enabled": true,
    "apiSeatAllocated": false
  }
]
```

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
