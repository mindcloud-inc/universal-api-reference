# Affinda: Get specific resthook subscription

Retrieves a specific resthook subscription from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-webhook?${params}`, {
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
| `id` | string | yes | Resthook subscription's ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "autoDeactivated": true,
      "autoDeactivateReason": "string",
      "event": "string",
      "id": 1,
      "organization": {},
      "targetUrl": "https://example.com",
      "version": "string",
      "workspace": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `autoDeactivated` | boolean |  |
| `autoDeactivateReason` | string |  |
| `event` | string |  |
| `id` | number |  |
| `organization` | object |  |
| `targetUrl` | string |  |
| `version` | string |  |
| `workspace` | object |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/resthook_subscriptions/:id` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

