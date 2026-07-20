# Linkbreakers: Identify Visitor

Identifies a visitor record within Linkbreakers.

```
POST https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/identify-visitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/identify-visitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/identify-visitor', {
  method: 'POST',
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
| `lbid` | string | no | LBID that initiated the visit. |
| `setOnce` | boolean | no | Only set fields that are currently empty. |
| `visitor` | object | no | Visitor identification payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": true,
      "visitor": {
        "attributes": {},
        "createdAt": "string",
        "devices": [
          {}
        ],
        "email": "ava@example.com",
        "events": [
          {}
        ],
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "links": [
          {}
        ],
        "phone": "string",
        "updatedAt": "string",
        "workspaceId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | boolean | Whether identification created a new visitor record. |
| `visitor` | object | Identified visitor profile. |
| `visitor.attributes` | object |  |
| `visitor.createdAt` | string |  |
| `visitor.devices` | array<object> |  |
| `visitor.email` | string |  |
| `visitor.events` | array<object> |  |
| `visitor.firstName` | string |  |
| `visitor.id` | string |  |
| `visitor.lastName` | string |  |
| `visitor.links` | array<object> |  |
| `visitor.phone` | string |  |
| `visitor.updatedAt` | string |  |
| `visitor.workspaceId` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `POST /v1/visitor/identify` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/identify-visitor.md) for the provider-specific parameters and requirements.

