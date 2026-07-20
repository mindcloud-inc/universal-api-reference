# Trolley: Delete Invoice

Deletes an existing invoice from Trolley.

```
DELETE https://connect.mindcloud.co/v1/universal/trolley/latest/actions/delete-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trolley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/delete-invoice?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trolley/latest/actions/delete-invoice?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |

## Native endpoint

Through the native Trolley API, this operation is `POST /v1/invoices/delete` (base URL `https://api.trolley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-invoice.md) for the provider-specific parameters and requirements.

