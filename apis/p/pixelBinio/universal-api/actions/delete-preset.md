# PixelBin.io: Delete Preset

Deletes an existing preset from PixelBin.io.

```
DELETE https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/delete-preset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/delete-preset?connectionId=$CONNECTION_ID&presetName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "presetName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/delete-preset?${params}`, {
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
| `archived` | boolean | Whether the preset was archived at delete time. |
| `createdAt` | date | Preset creation timestamp. |
| `isActive` | boolean | Whether the preset was active at delete time. |
| `presetName` | string | Preset name. |
| `transformation` | string | Transformation chain for the preset. |
| `updatedAt` | date | Preset update timestamp. |

## Native endpoint

Through the native PixelBin.io API, this operation is `DELETE /service/platform/assets/v1.0/presets/:presetName` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-preset.md) for the provider-specific parameters and requirements.

