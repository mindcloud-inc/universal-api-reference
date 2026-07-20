# Zite: List Records

Retrieves records from a specific Zite table.

```
GET https://connect.mindcloud.co/v1/universal/zite/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zite/latest/actions/list-records?connectionId=$CONNECTION_ID&databaseId=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zite/latest/actions/list-records?${params}`, {
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
| `databaseId` | string | yes |  |
| `tableId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "data": {},
      "fields": {},
      "id": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `data` | object |  |
| `fields` | object |  |
| `id` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Zite API, this operation is `POST /bases/:databaseId/tables/:tableId/records/list` (base URL `https://tables.fillout.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.

