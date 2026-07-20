# xMatters: Set scenario sender permissions

Sets scenario sender permissions in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/set-scenario-sender-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/set-scenario-sender-permissions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/set-scenario-sender-permissions', {
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
| `scenarioId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "editScenarios": true,
          "sender": {
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "name": "Ava Chen",
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "senderType": "string"
        }
      ],
      "links": {
        "self": "https://example.com"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].editScenarios` | boolean |  |
| `data[].sender.firstName` | string |  |
| `data[].sender.id` | string |  |
| `data[].sender.lastName` | string |  |
| `data[].sender.links.self` | string |  |
| `data[].sender.name` | string |  |
| `data[].sender.recipientType` | string |  |
| `data[].sender.targetName` | string |  |
| `data[].senderType` | string |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `PUT scenarios/{scenarioId}/sender-permissions` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-scenario-sender-permissions.md) for the provider-specific parameters and requirements.

