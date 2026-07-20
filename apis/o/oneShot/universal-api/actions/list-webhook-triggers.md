# 1Shot: List Webhook Triggers

Retrieves webhook trigger types from 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-webhook-triggers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-webhook-triggers?connectionId=$CONNECTION_ID&businessId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-webhook-triggers?${params}`, {
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
| `businessId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": "string",
      "contractMethodIds": [
        "string"
      ],
      "created": 1,
      "deleted": true,
      "description": "string",
      "endpointId": "string",
      "events": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "service": "string",
      "updated": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | string |  |
| `contractMethodIds[]` | string |  |
| `created` | number |  |
| `deleted` | boolean |  |
| `description` | string |  |
| `endpointId` | string |  |
| `events[]` | string |  |
| `id` | string |  |
| `name` | string |  |
| `service` | string |  |
| `updated` | number |  |
| `userId` | string |  |

## Native endpoint

Through the native 1Shot API, this operation is `GET /business/:businessId/webhooks/triggers` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-triggers.md) for the provider-specific parameters and requirements.

