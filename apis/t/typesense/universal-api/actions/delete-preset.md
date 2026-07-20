# Typesense: Delete Preset

Deletes a search preset from Typesense.

```
DELETE https://connect.mindcloud.co/v1/universal/typesense/latest/actions/delete-preset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/delete-preset?connectionId=$CONNECTION_ID&presetName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "presetName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typesense/latest/actions/delete-preset?${params}`, {
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
| `presetName` | string | yes | Preset name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `response` | object |  |

## Native endpoint

Through the native Typesense API, this operation is `DELETE /presets/{{presetName}}` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-preset.md) for the provider-specific parameters and requirements.

