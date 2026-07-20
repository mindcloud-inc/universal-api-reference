# Luxafor: Set Solid Custom Color

Updates a Luxafor device to a custom solid color.

```
PUT https://connect.mindcloud.co/v1/universal/luxafor/latest/actions/set-solid-custom-color
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Luxafor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/luxafor/latest/actions/set-solid-custom-color" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionFields.customColor": "ff0000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/luxafor/latest/actions/set-solid-custom-color', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionFields.customColor": "ff0000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionFields` | object | no |  |
| `actionFields.customColor` | string | yes | Six-character hexadecimal color code. Use 000000 to turn the device off. Example: `ff0000`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Luxafor API returns.

## Native endpoint

Through the native Luxafor API, this operation is `POST /solid_color` (base URL `https://api.luxafor.com/webhook/v1/actions`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-solid-custom-color.md) for the provider-specific parameters and requirements.

