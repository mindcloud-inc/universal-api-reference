# Jodoo: Create Records



```
POST https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/create-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/create-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "69c4042cce7f5503d03455c1",
  "entryId": "63e809d2b8c3070007093940",
  "dataList": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/create-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "69c4042cce7f5503d03455c1",
    "entryId": "63e809d2b8c3070007093940",
    "dataList": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Jodoo app ID that owns the form. Example: `69c4042cce7f5503d03455c1`. |
| `entryId` | string | yes | Jodoo form ID to create records in. Example: `63e809d2b8c3070007093940`. |
| `dataList` | object<object> | yes | JSON array of record payload objects for Jodoo `data_list`. Each record must be keyed by widget IDs, and every widget value must be wrapped in an object with a `value` property. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "successCount": 1,
      "successIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `successCount` | number |  |
| `successIds[]` | string |  |

## Native endpoint

Through the native Jodoo API, this operation is `POST /app/entry/data/batch_create` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-records.md) for the provider-specific parameters and requirements.

