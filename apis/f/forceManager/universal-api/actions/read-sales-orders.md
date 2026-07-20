# ForceManager: Read Sales Orders

Retrieves sales orders from your ForceManager account.

```
GET https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-sales-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-sales-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-sales-orders?${params}`, {
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
      "accountId": 1,
      "address": "string",
      "comments": "string",
      "contactId": 1,
      "id": 1,
      "statusId": 1,
      "topic": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | Account identifier linked to the sales order. |
| `address` | string | Address line. |
| `comments` | string | Comments of the sales order. |
| `contactId` | number | Contact identifier linked to the sales order. |
| `id` | number | Unique identifier for the sales order. |
| `statusId` | number | Status identifier linked to the sales order. |
| `topic` | string | Topic of the sales order. |

## Native endpoint

Through the native ForceManager API, this operation is `GET /salesorder`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-sales-orders.md) for the provider-specific parameters and requirements.

