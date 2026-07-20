# Vestaboard: Set Transition

Updates transition settings in Vestaboard.

```
PUT https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/set-transition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vestaboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/set-transition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transition": "classic",
  "transitionSpeed": "fast"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vestaboard/latest/actions/set-transition', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transition": "classic",
    "transitionSpeed": "fast"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transition` | list | yes | Transition style to apply. One of: `classic`, `curtain`, `drift`, `wave`. |
| `transitionSpeed` | list | yes | Transition speed to apply. One of: `fast`, `gentle`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "transition": "string",
      "transitionSpeed": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `transition` | string | Updated transition style for the device. |
| `transitionSpeed` | string | Updated transition speed for the device. |

## Native endpoint

Through the native Vestaboard API, this operation is `PUT /transition` (base URL `https://cloud.vestaboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-transition.md) for the provider-specific parameters and requirements.

