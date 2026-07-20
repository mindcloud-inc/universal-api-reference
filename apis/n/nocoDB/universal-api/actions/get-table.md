# NocoDB: Get Table

Retrieves table schema details from NocoDB.

```
GET https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/get-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NocoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/get-table?connectionId=$CONNECTION_ID&baseId=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseId": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nocoDB/latest/actions/get-table?${params}`, {
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
| `tableId` | string | yes | Table identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseId": "string",
      "displayFieldId": "string",
      "fields": [
        {}
      ],
      "id": "string",
      "meta": {},
      "sourceId": "string",
      "title": "string",
      "views": [
        {}
      ],
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
| `displayFieldId` | string |  |
| `fields` | array<object> |  |
| `id` | string |  |
| `meta` | object |  |
| `sourceId` | string |  |
| `title` | string |  |
| `views` | array<object> |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native NocoDB API, this operation is `GET /api/v3/meta/bases/:baseId/tables/:tableId` (base URL `https://app.nocodb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table.md) for the provider-specific parameters and requirements.

