# NocoDB: Get Base

Retrieves details for a base from NocoDB.

```
GET https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/get-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/get-base?connectionId=$CONNECTION_ID&baseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/get-base?${params}`, {
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
| `baseId` | string | yes | Base identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": "string",
      "meta": {},
      "sources": [
        {}
      ],
      "title": "string",
      "updated_at": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | string |  |
| `meta` | object |  |
| `sources` | array<object> |  |
| `title` | string |  |
| `updated_at` | string |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native NocoDB API, this operation is `GET /api/v3/meta/bases/:baseId` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-base.md) for the provider-specific parameters and requirements.

