# Jodoo: Delete Records



```
DELETE https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/delete-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/delete-records?connectionId=$CONNECTION_ID&appId=69c4042cce7f5503d03455c1&entryId=63e809d2b8c3070007093940&dataIds=69c41718ccf94767d8ebcd09%2C69c41718ccf94767d8ebcd0a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "69c4042cce7f5503d03455c1",
  "entryId": "63e809d2b8c3070007093940",
  "dataIds": "69c41718ccf94767d8ebcd09,69c41718ccf94767d8ebcd0a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/delete-records?${params}`, {
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
| `appId` | string | yes | Jodoo app ID that owns the form. Example: `69c4042cce7f5503d03455c1`. |
| `entryId` | string | yes | Jodoo form ID that owns the records. Example: `63e809d2b8c3070007093940`. |
| `dataIds` | object<string> | yes | JSON array of record IDs for Jodoo `data_ids`. Example: `69c41718ccf94767d8ebcd09,69c41718ccf94767d8ebcd0a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "successCount": 1
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

## Native endpoint

Through the native Jodoo API, this operation is `POST /app/entry/data/batch_delete` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-records.md) for the provider-specific parameters and requirements.

