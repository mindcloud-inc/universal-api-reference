# Encodian - Sign: Create Trigr Webhook Subscription



```
POST https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/create-trigr-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/create-trigr-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "callbackUrl": "https://example.com",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/create-trigr-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "callbackUrl": "https://example.com",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callbackUrl` | string | yes | Webhook callback URL that Encodian Trigr should call. |
| `title` | string | yes | Title of the Encodian Trigr webhook subscription. |
| `description` | string | no | Description of the Trigr webhook subscription purpose. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "success": true,
      "tenantWebHookId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> | Errors returned by Encodian. |
| `HttpStatusCode` | number | HTTP status code for the response. |
| `HttpStatusMessage` | string | HTTP status message for the response. |
| `success` | boolean | Whether webhook subscription management succeeded. |
| `tenantWebHookId` | number | ID of the webhook subscription. |

## Native endpoint

Through the native Encodian - Sign API, this operation is `POST /api/v1/Trigr/ManageWebHook` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-trigr-webhook-subscription.md) for the provider-specific parameters and requirements.

