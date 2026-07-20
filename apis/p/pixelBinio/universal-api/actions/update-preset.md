# PixelBin.io: Update Preset

Updates an existing preset in PixelBin.io.

```
PUT https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/update-preset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/update-preset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "archived": true,
  "presetName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/update-preset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "archived": true,
    "presetName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `archived` | boolean | yes |  |
| `presetName` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "isActive": true,
      "presetName": "Ava Chen",
      "transformation": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | PixelBin preset identifier. |
| `archived` | boolean | Whether the preset is archived. |
| `createdAt` | date | Preset creation timestamp. |
| `isActive` | boolean | Whether the preset is active. |
| `presetName` | string | Preset name. |
| `transformation` | string | Transformation chain for the preset. |
| `updatedAt` | date | Preset update timestamp. |

## Native endpoint

Through the native PixelBin.io API, this operation is `PATCH /service/platform/assets/v1.0/presets/:presetName` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-preset.md) for the provider-specific parameters and requirements.

