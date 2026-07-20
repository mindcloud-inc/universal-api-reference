# Open Letter Connect: Get Order Details

Retrieves order details from Open Letter Connect.

```
GET https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-order-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-order-details?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-order-details?${params}`, {
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
| `id` | number | yes | The numeric order ID from Open Letter Connect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancellationWindow": "string",
      "cost": 1,
      "costAdditionalPage": 1,
      "costGsv": 1,
      "costRos": 1,
      "deliverableContacts": 1,
      "dncContacts": "string",
      "orderCost": 1,
      "perMailerAdditionalPageCost": 1,
      "perMailerCost": 1,
      "perMailerGsvCost": 1,
      "perMailerRosCost": 1,
      "totalContacts": 1,
      "unDeliverableContacts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancellationWindow` | string |  |
| `cost` | number |  |
| `costAdditionalPage` | number |  |
| `costGsv` | number |  |
| `costRos` | number |  |
| `deliverableContacts` | number |  |
| `dncContacts` | string |  |
| `orderCost` | number |  |
| `perMailerAdditionalPageCost` | number |  |
| `perMailerCost` | number |  |
| `perMailerGsvCost` | number |  |
| `perMailerRosCost` | number |  |
| `totalContacts` | number |  |
| `unDeliverableContacts` | number |  |

## Native endpoint

Through the native Open Letter Connect API, this operation is `GET /orders/detail/:id` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-details.md) for the provider-specific parameters and requirements.

