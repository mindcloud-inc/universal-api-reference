# Instructure: Update Custom Color

Updates a custom color in Instructure Canvas.

```
PUT https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-custom-color
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-custom-color" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assetString": "string",
  "hexcode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-custom-color', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assetString": "string",
    "hexcode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assetString` | string | yes | Asset string for the custom color entry. |
| `hexcode` | string | yes | Hex color code to assign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hexcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hexcode` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `PUT /users/self/colors/:asset_string` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-color.md) for the provider-specific parameters and requirements.

