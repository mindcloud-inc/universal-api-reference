# xMatters: Create a communication plan

Creates a communication plan in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-communication-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-communication-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-communication-plan', {
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
| `accessibleByAll` | boolean | no |  |
| `enabled` | boolean | no |  |
| `floodControl` | boolean | no |  |
| `name` | string | no |  |
| `position` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessibleByAll": true,
      "created": "2026-05-07T12:00:00.000Z",
      "creator": {
        "externallyOwned": true,
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "targetName": "Ava Chen"
      },
      "description": "string",
      "enabled": true,
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "position": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessibleByAll` | boolean |  |
| `created` | date |  |
| `creator.externallyOwned` | boolean |  |
| `creator.firstName` | string |  |
| `creator.id` | string |  |
| `creator.lastName` | string |  |
| `creator.links.self` | string |  |
| `creator.recipientType` | string |  |
| `creator.targetName` | string |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `links.self` | string |  |
| `name` | string |  |
| `position` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `POST plans` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-communication-plan.md) for the provider-specific parameters and requirements.

