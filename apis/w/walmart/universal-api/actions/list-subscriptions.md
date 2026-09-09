# Walmart: List Subscriptions

Retrieve details of all webhook subscriptions you've created.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-subscriptions?${params}`, {
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
| `status` | list<string> | no | Filter results by subscription status. Allowed values: `ACTIVE`, `INACTIVE` |
| `eventType` | list<string> | no | Filter results to a specific event type. Refer to the events section for the list of available event types. |
| `resourceName` | string | no | Filter results to a specific resource (functional category) that the event type maps to. Refer to the events section for the list of available resource names. |
| `subscriptionId` | string | no | Filter results to a specific subscription by its unique identifier. |

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
      "eventType": "string",
      "eventUrl": "https://example.com",
      "eventVersion": "string",
      "headers": {
        "contentType": "string"
      },
      "partnerId": "string",
      "resourceName": "Ava Chen",
      "status": "string",
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
| `eventType` | string |  |
| `eventUrl` | string |  |
| `eventVersion` | string |  |
| `headers.contentType` | string |  |
| `partnerId` | string |  |
| `resourceName` | string |  |
| `status` | string |  |
| `subscriptionId` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/webhooks/subscriptions` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

