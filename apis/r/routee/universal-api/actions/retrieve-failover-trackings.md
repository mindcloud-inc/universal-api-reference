# Routee: Retrieve Failover trackings

Retrieves failover tracking records from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-failover-trackings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-failover-trackings?connectionId=$CONNECTION_ID&trackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-failover-trackings?${params}`, {
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
| `trackingId` | string | yes | The tracking Id of a failover message |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationId": "string",
      "createdAt": "string",
      "messages": [
        [
          {}
        ]
      ],
      "originatingService": "string",
      "status": "string",
      "terminationChannel": "string",
      "totalPrice": 1,
      "trackingId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationId` | string |  |
| `createdAt` | string |  |
| `messages[]` | array<object> |  |
| `messages[].body` | object |  |
| `messages[].body.action` | object |  |
| `messages[].body.action.caption` | string |  |
| `messages[].body.action.targetUrl` | string |  |
| `messages[].body.text` | string |  |
| `messages[].country` | string |  |
| `messages[].createdAt` | string |  |
| `messages[].expiredOnDeliveryAt` | string |  |
| `messages[].expireOnDelivery` | boolean |  |
| `messages[].failoverOnStatuses[]` | array<string> |  |
| `messages[].from` | string |  |
| `messages[].inboundUrl` | string |  |
| `messages[].order` | number |  |
| `messages[].price` | number |  |
| `messages[].status` | object |  |
| `messages[].status.name` | string |  |
| `messages[].status.reason` | object |  |
| `messages[].status.reason.description` | string |  |
| `messages[].status.reason.detailedStatus` | string |  |
| `messages[].status.updatedDate` | string |  |
| `messages[].to` | string |  |
| `messages[].trackingId` | string |  |
| `messages[].ttl` | number |  |
| `messages[].type` | string |  |
| `originatingService` | string |  |
| `status` | string |  |
| `terminationChannel` | string |  |
| `totalPrice` | number |  |
| `trackingId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /failover/tracking/:trackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-failover-trackings.md) for the provider-specific parameters and requirements.

