# LightwaveRF Power: Update Favourite

Updates an existing favourite in LightwaveRF Power.

```
PUT https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/update-favourite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Power `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/update-favourite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "favouriteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/update-favourite', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "favouriteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `favouriteId` | string | yes | The LightwaveRF favourite identifier to update. |
| `order[]` | array<string> | no | The ordered list of feature set identifiers for the favourite. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupId": "string",
      "name": "Ava Chen",
      "order": [
        "string"
      ],
      "parentGroups": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupId` | string |  |
| `name` | string |  |
| `order` | array<string> |  |
| `parentGroups` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native LightwaveRF Power API, this operation is `PUT /v1/favourite/{favouriteId}` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-favourite.md) for the provider-specific parameters and requirements.

