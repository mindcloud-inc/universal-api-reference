# SureCart: Retrieve Subscription



```
GET https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-subscription?connectionId=$CONNECTION_ID&id=cc7985b7-6738-45e2-8910-146bc0582404" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "cc7985b7-6738-45e2-8910-146bc0582404"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-subscription?${params}`, {
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
| `id` | string | yes | The subscription ID to retrieve. Example: `cc7985b7-6738-45e2-8910-146bc0582404`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelAtPeriodEnd": true,
      "createdAt": 1,
      "currency": "string",
      "currentCancellationAct": "string",
      "currentPeriod": "string",
      "currentPeriodEndAt": 1,
      "currentPeriodStartAt": 1,
      "customer": "string",
      "endBehavior": "string",
      "id": "string",
      "liveMode": true,
      "manualPayment": true,
      "metadata": {},
      "object": "string",
      "pendingUpdate": {},
      "portalUrl": "https://example.com",
      "price": "string",
      "purchase": "string",
      "quantity": 1,
      "status": "string",
      "subtotalAmount": 1,
      "taxEnabled": true,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelAtPeriodEnd` | boolean |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `currentCancellationAct` | string |  |
| `currentPeriod` | string |  |
| `currentPeriodEndAt` | number |  |
| `currentPeriodStartAt` | number |  |
| `customer` | string |  |
| `endBehavior` | string |  |
| `id` | string |  |
| `liveMode` | boolean |  |
| `manualPayment` | boolean |  |
| `metadata` | object |  |
| `object` | string |  |
| `pendingUpdate` | object |  |
| `portalUrl` | string |  |
| `price` | string |  |
| `purchase` | string |  |
| `quantity` | number |  |
| `status` | string |  |
| `subtotalAmount` | number |  |
| `taxEnabled` | boolean |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native SureCart API, this operation is `GET v1/subscriptions/:id` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-subscription.md) for the provider-specific parameters and requirements.

