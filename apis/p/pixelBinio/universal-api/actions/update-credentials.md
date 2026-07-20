# PixelBin.io: Update Transformation Module Credentials

Updates transformation module credentials in PixelBin.io.

```
PUT https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/update-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/update-credentials" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "credentials": {},
  "pluginId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/update-credentials', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "credentials": {},
    "pluginId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `credentials` | object | yes | Replacement credential object for the transformation module. |
| `pluginId` | string | yes | Transformation module identifier whose credentials you want to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credentials": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credentials` | object | Updated transformation module credentials returned by PixelBin. |

## Native endpoint

Through the native PixelBin.io API, this operation is `PATCH /service/platform/assets/v1.0/credentials/:pluginId` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-credentials.md) for the provider-specific parameters and requirements.

