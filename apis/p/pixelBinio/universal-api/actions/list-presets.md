# PixelBin.io: List Presets

Retrieves preset records from your PixelBin.io account.

```
GET https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/list-presets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/list-presets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/list-presets?${params}`, {
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
| `archived` | boolean | no | Filter presets by archive state. |
| `name` | string | no | Filter presets by name. |
| `pageNo` | number | no | Preset results page number. |
| `pageSize` | number | no | Preset results page size. |
| `transformation` | string | no | Filter presets by transformation chain. |

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

Through the native PixelBin.io API, this operation is `GET /service/platform/assets/v1.0/presets` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-presets.md) for the provider-specific parameters and requirements.

