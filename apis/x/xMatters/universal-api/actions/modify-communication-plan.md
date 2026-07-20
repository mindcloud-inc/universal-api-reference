# xMatters: Modify communication plan

Updates communication plan in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-communication-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-communication-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-communication-plan', {
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
| `accessibleByAll` | boolean | no |  |
| `description` | string | no |  |
| `enabled` | boolean | no |  |
| `floodControl` | boolean | no |  |
| `id` | string | no |  |
| `loggingLevel` | string | no |  |
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
      "loggingLevel": "string",
      "name": "Ava Chen",
      "planType": "string",
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
| `loggingLevel` | string |  |
| `name` | string |  |
| `planType` | string |  |
| `position` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `POST plans` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-communication-plan.md) for the provider-specific parameters and requirements.

