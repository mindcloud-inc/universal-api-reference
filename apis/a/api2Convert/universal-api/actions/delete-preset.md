# Api2Convert: Delete Preset

Deletes an existing preset from Api2Convert.

```
DELETE https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/delete-preset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/delete-preset?connectionId=$CONNECTION_ID&presetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "presetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/delete-preset?${params}`, {
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
| `presetId` | string | yes | Unique identifier of the preset to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "message": "string",
      "preset_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the preset was deleted. |
| `message` | string | Deletion result message. |
| `preset_id` | string | Identifier of the deleted preset. |

## Native endpoint

Through the native Api2Convert API, this operation is `DELETE /presets/:preset_id` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-preset.md) for the provider-specific parameters and requirements.

