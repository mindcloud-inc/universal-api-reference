# Signaturit: List Signatures

Retrieves signatures from Signaturit.

```
GET https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-signatures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Signaturit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-signatures?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-signatures?${params}`, {
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
| `limit` | number | no | Maximum number of signatures to return. Default: `100`. Example: `100`. |
| `offset` | number | no | Results offset. Default: `0`. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "documents": [
        {
          "created_at": "string",
          "email": "ava@example.com",
          "events": [
            {
              "created_at": "string",
              "reason": "string",
              "type": "string"
            }
          ],
          "file": {
            "name": "Ava Chen",
            "pages": 1,
            "size": 1
          },
          "id": "string",
          "name": "Ava Chen",
          "status": "string"
        }
      ],
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `documents[].created_at` | string |  |
| `documents[].email` | string |  |
| `documents[].events[].created_at` | string |  |
| `documents[].events[].reason` | string |  |
| `documents[].events[].type` | string |  |
| `documents[].file.name` | string |  |
| `documents[].file.pages` | number |  |
| `documents[].file.size` | number |  |
| `documents[].id` | string |  |
| `documents[].name` | string |  |
| `documents[].status` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Signaturit API, this operation is `GET /signatures.json` (base URL `https://api.sandbox.signaturit.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-signatures.md) for the provider-specific parameters and requirements.

