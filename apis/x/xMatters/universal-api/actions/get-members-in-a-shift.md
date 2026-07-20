# xMatters: Get members in a shift

Retrieves members in a shift from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-members-in-a-shift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-members-in-a-shift?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-members-in-a-shift?${params}`, {
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
| `groupId` | string | no |  |
| `shiftId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "delay": 1,
          "escalationType": "string",
          "position": 1,
          "recipient": {
            "firstName": "Ava",
            "id": "string",
            "inRotation": true,
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "onDuty": true,
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "shift": {
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "name": "Ava Chen"
          }
        }
      ],
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
| `data[].delay` | number |  |
| `data[].escalationType` | string |  |
| `data[].position` | number |  |
| `data[].recipient.firstName` | string |  |
| `data[].recipient.id` | string |  |
| `data[].recipient.inRotation` | boolean |  |
| `data[].recipient.lastName` | string |  |
| `data[].recipient.links.self` | string |  |
| `data[].recipient.onDuty` | boolean |  |
| `data[].recipient.recipientType` | string |  |
| `data[].recipient.targetName` | string |  |
| `data[].shift.id` | string |  |
| `data[].shift.links.self` | string |  |
| `data[].shift.name` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET groups/{groupId}/shifts/{shiftId}/members` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-members-in-a-shift.md) for the provider-specific parameters and requirements.

