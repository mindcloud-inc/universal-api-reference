# xMatters: Modify a plan endpoint

Updates a plan endpoint in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-plan-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-plan-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-plan-endpoint', {
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
| `authentication` | string | no |  |
| `authenticationType` | string | no |  |
| `endpointType` | string | no |  |
| `id` | string | no |  |
| `name` | string | no |  |
| `planId` | string | no |  |
| `url` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authentication": {
        "oauthTokenUrl": "https://example.com",
        "username": "Ava Chen"
      },
      "authenticationType": "string",
      "endpointType": "string",
      "id": "string",
      "link": {
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "plan": {
        "id": "string"
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authentication.oauthTokenUrl` | string |  |
| `authentication.username` | string |  |
| `authenticationType` | string |  |
| `endpointType` | string |  |
| `id` | string |  |
| `link.self` | string |  |
| `name` | string |  |
| `plan.id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST plans/{planId}/endpoints` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-a-plan-endpoint.md) for the provider-specific parameters and requirements.

