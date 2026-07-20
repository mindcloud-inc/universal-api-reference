# xMatters: Modify an Integration

Updates an Integration in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-an-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-an-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-an-integration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deployed` | boolean | no |  |
| `id` | string | no |  |
| `planId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deployed": true,
      "endpoint": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "plan": {
          "id": "string",
          "links": {
            "self": "https://example.com"
          }
        }
      },
      "environment": "string",
      "form": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        }
      },
      "id": "string",
      "integrationType": "string",
      "name": "Ava Chen",
      "operation": "string",
      "plan": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        }
      },
      "triggeredBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deployed` | boolean |  |
| `endpoint.id` | string |  |
| `endpoint.links.self` | string |  |
| `endpoint.plan.id` | string |  |
| `endpoint.plan.links.self` | string |  |
| `environment` | string |  |
| `form.id` | string |  |
| `form.links.self` | string |  |
| `id` | string |  |
| `integrationType` | string |  |
| `name` | string |  |
| `operation` | string |  |
| `plan.id` | string |  |
| `plan.links.self` | string |  |
| `triggeredBy` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST plans/{planId}/integrations` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-an-integration.md) for the provider-specific parameters and requirements.

