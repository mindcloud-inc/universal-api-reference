# Ragic: Mass Search And Replace

Replaces matching values across multiple Ragic records.

```
PUT https://connect.mindcloud.co/v1/universal/ragic/latest/actions/mass-search-and-replace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ragic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/mass-search-and-replace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tabFolderPath": "string",
  "sheetIndex": 1,
  "action[0].field": "609",
  "action[0].valueReplaced": "Stage3BulkValue",
  "action[0].valueNew": "Stage3BulkFinal"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ragic/latest/actions/mass-search-and-replace', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tabFolderPath": "string",
    "sheetIndex": 1,
    "action[0].field": "609",
    "action[0].valueReplaced": "Stage3BulkValue",
    "action[0].valueNew": "Stage3BulkFinal"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tabFolderPath` | string | yes |  |
| `sheetIndex` | number | yes |  |
| `recordId` | number | no |  |
| `action[0].field` | number | yes | Example: `609`. |
| `action[0].valueReplaced` | string | yes | Example: `Stage3BulkValue`. |
| `action[0].valueNew` | string | yes | Example: `Stage3BulkFinal`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `where` | string | no | Example: `1,eq,apps@mindcloud.co`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskId` | string | Asynchronous Ragic task identifier returned by the mass search-and-replace request. |

## Native endpoint

Through the native Ragic API, this operation is `POST /:tabFolderPath/:sheetIndex/massOperation/massSearchReplace` (base URL `{{credentials.serverUrl}}/mindcloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mass-search-and-replace.md) for the provider-specific parameters and requirements.

