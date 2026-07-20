# NocoDB: List Tables

Retrieves tables in a NocoDB base.

```
GET https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-tables?connectionId=$CONNECTION_ID&baseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/list-tables?${params}`, {
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
      "baseId": "string",
      "id": "string",
      "meta": {},
      "title": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseId` | string |  |
| `id` | string |  |
| `meta` | object |  |
| `title` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native NocoDB API, this operation is `GET /api/v3/meta/bases/:baseId/tables` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tables.md) for the provider-specific parameters and requirements.

