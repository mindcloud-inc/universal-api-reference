# Walmart: Update Subscription

Update the details of a subscription.

```
POST https://connect.mindcloud.co/v1/universal/walmart/latest/actions/update-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/update-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/update-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authDetails.authMethod` | list<string> | no |  |
| `status` | list<string> | no | Filter results by subscription status. Allowed values: `ACTIVE`, `INACTIVE` |
| `authDetails.userName` | string | no |  |
| `eventUrl` | string | no | Destination URL where notifications are delivered. |
| `authDetails.password` | string | no |  |
| `subscriptionId` | string | yes | The unique identifier of the subscription to update. |
| `authDetails` | object | no |  |
| `authDetails.authUrl` | string | no | OAuth server or token URL used when the authentication method is OAUTH. |
| `authDetails.clientSecret` | string | no | Client secret used with the OAuth server (OAUTH) or as key material for HMAC. |
| `authDetails.clientId` | string | no | Client ID used with the OAuth server when the authentication method is OAUTH. |
| `authDetails.authHeaderName` | string | no | Header name used to pass the authorization value to the destination URL (for example, `Authorization`). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authDetails": {
        "authHeaderName": "Ava Chen",
        "authMethod": "string",
        "password": "string",
        "userName": "Ava Chen"
      },
      "channelType": "string",
      "eventType": "string",
      "eventUrl": "https://example.com",
      "eventVersion": "string",
      "partnerId": "string",
      "resourceName": "Ava Chen",
      "status": "string",
      "subscribedBy": "string",
      "subscriptionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authDetails.authHeaderName` | string |  |
| `authDetails.authMethod` | string |  |
| `authDetails.password` | string |  |
| `authDetails.userName` | string |  |
| `channelType` | string |  |
| `eventType` | string |  |
| `eventUrl` | string |  |
| `eventVersion` | string |  |
| `partnerId` | string |  |
| `resourceName` | string |  |
| `status` | string |  |
| `subscribedBy` | string |  |
| `subscriptionId` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `PATCH /v3/webhooks/subscriptions/:subscriptionId` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscription.md) for the provider-specific parameters and requirements.

