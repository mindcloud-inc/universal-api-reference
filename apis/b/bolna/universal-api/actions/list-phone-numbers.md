# Bolna: List Phone Numbers

Retrieves phone numbers configured in your Bolna account.

```
GET https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-phone-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-phone-numbers?${params}`, {
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
      "agentId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "humanizedCreatedAt": "string",
      "humanizedUpdatedAt": "string",
      "id": "string",
      "phoneNumber": "string",
      "price": "string",
      "renewalAt": "string",
      "rented": true,
      "telephonyProvider": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string |  |
| `createdAt` | date |  |
| `humanizedCreatedAt` | string |  |
| `humanizedUpdatedAt` | string |  |
| `id` | string |  |
| `phoneNumber` | string |  |
| `price` | string |  |
| `renewalAt` | string |  |
| `rented` | boolean |  |
| `telephonyProvider` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Bolna API, this operation is `GET /phone-numbers/all` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-phone-numbers.md) for the provider-specific parameters and requirements.

