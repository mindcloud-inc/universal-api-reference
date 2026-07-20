# Signaturit: List Certified Emails

Retrieves certified emails from Signaturit.

```
GET https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-certified-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Signaturit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-certified-emails?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-certified-emails?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Max number of emails to retrieve. Default: `100`. Example: `100`. |
| `offset` | number | no | Results offset. Default: `0`. Example: `0`. |
| `status` | string | no | Filter emails by status. Example: `sent`. |
| `since` | string | no | Return emails sent on or after this date. Example: `2026-03-18`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "certificates": [
        {
          "created_at": "string",
          "email": "ava@example.com",
          "events": [
            {
              "created_at": "string",
              "type": "string"
            }
          ],
          "file": {
            "name": "Ava Chen",
            "size": 1
          },
          "id": "string",
          "name": "Ava Chen",
          "status": "string"
        }
      ],
      "created_at": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certificates[].created_at` | string |  |
| `certificates[].email` | string |  |
| `certificates[].events[].created_at` | string |  |
| `certificates[].events[].type` | string |  |
| `certificates[].file.name` | string |  |
| `certificates[].file.size` | number |  |
| `certificates[].id` | string |  |
| `certificates[].name` | string |  |
| `certificates[].status` | string |  |
| `created_at` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Signaturit API, this operation is `GET /emails.json` (base URL `https://api.sandbox.signaturit.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-certified-emails.md) for the provider-specific parameters and requirements.

