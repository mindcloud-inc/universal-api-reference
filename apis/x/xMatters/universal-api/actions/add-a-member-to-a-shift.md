# xMatters: Add a member to a shift

Adds a member to a shift in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-member-to-a-shift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-member-to-a-shift" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-member-to-a-shift', {
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
| `delay` | number | no |  |
| `escalationType` | string | no |  |
| `groupId` | string | no |  |
| `inRotation` | boolean | no |  |
| `onDuty` | boolean | no |  |
| `position` | number | no |  |
| `recipient` | string | no |  |
| `shiftId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "delay": 1,
      "escalationType": "string",
      "inRotation": true,
      "onDuty": true,
      "position": 1,
      "recipient": {
        "id": "string",
        "recipientType": "string"
      },
      "shift": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `delay` | number |  |
| `escalationType` | string |  |
| `inRotation` | boolean |  |
| `onDuty` | boolean |  |
| `position` | number |  |
| `recipient.id` | string |  |
| `recipient.recipientType` | string |  |
| `shift.id` | string |  |
| `shift.links.self` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST groups/{groupId}/shifts/{shiftId}/members` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-a-member-to-a-shift.md) for the provider-specific parameters and requirements.

