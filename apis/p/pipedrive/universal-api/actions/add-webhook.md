# Pipedrive: Add Webhook

Creates a new webhook in Pipedrive.

```
POST https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionUrl": "https://example.com",
  "eventAction": "string",
  "eventObject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/add-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionUrl": "https://example.com",
    "eventAction": "string",
    "eventObject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionUrl` | string | yes | HTTPS callback URL to receive webhook payloads. |
| `eventAction` | string | yes | Webhook event action: added, updated, deleted, *. |
| `eventObject` | string | yes | Webhook event object: deal, person, organization, activity, note, product, lead, etc. |
| `version` | string | no | Webhook API version. Default: `2.0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addTime": "string",
      "companyId": 1,
      "eventAction": "string",
      "eventObject": "string",
      "httpAuthPassword": {},
      "httpAuthUser": {},
      "id": 1,
      "isActive": 1,
      "name": {},
      "ownerId": 1,
      "removeReason": {},
      "removeTime": {},
      "subscriptionUrl": "https://example.com",
      "type": "string",
      "userId": 1,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addTime` | string |  |
| `companyId` | number |  |
| `eventAction` | string |  |
| `eventObject` | string |  |
| `httpAuthPassword` | object |  |
| `httpAuthUser` | object |  |
| `id` | number |  |
| `isActive` | number |  |
| `name` | object |  |
| `ownerId` | number |  |
| `removeReason` | object |  |
| `removeTime` | object |  |
| `subscriptionUrl` | string |  |
| `type` | string |  |
| `userId` | number |  |
| `version` | string |  |

## Native endpoint

Through the native Pipedrive API, this operation is `POST v1/webhooks` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-webhook.md) for the provider-specific parameters and requirements.

