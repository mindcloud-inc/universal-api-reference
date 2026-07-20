# Fillout: Get Record By Id

Retrieves a record from Fillout by ID.

```
GET https://connect.mindcloud.co/v1/universal/fillout/latest/actions/get-record-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fillout/latest/actions/get-record-by-id?connectionId=$CONNECTION_ID&databaseId=string&tableId=string&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "tableId": "string",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fillout/latest/actions/get-record-by-id?${params}`, {
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
| `databaseId` | string | yes | The database identifier. |
| `tableId` | string | yes | The table identifier. |
| `recordId` | string | yes | The record identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "data": {},
      "fields": {},
      "id": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `data` | object |  |
| `fields` | object |  |
| `id` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Fillout API, this operation is `GET https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record-by-id.md) for the provider-specific parameters and requirements.

