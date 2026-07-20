# InvoiceBerry: Update Item



```
PUT https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/update-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InvoiceBerry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/update-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/update-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native InvoiceBerry API, this operation is `POST /api` (base URL `https://www.invoiceberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item.md) for the provider-specific parameters and requirements.

