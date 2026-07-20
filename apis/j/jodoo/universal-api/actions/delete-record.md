# Jodoo: Delete Record



```
DELETE https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/delete-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/delete-record?connectionId=$CONNECTION_ID&appId=69c4042cce7f5503d03455c1&entryId=63e809d2b8c3070007093940&dataId=69c4042cce7f5503d034561b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "69c4042cce7f5503d03455c1",
  "entryId": "63e809d2b8c3070007093940",
  "dataId": "69c4042cce7f5503d034561b"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/delete-record?${params}`, {
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
| `entryId` | string | yes | Jodoo form ID that owns the record. Example: `63e809d2b8c3070007093940`. |
| `dataId` | string | yes | Jodoo record ID to delete. Example: `69c4042cce7f5503d034561b`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Jodoo API, this operation is `POST /app/entry/data/delete` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-record.md) for the provider-specific parameters and requirements.

