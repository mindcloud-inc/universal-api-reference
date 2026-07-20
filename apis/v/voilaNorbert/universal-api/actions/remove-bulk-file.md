# VoilaNorbert: Remove Bulk File

Deletes a bulk file from VoilaNorbert.

```
DELETE https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/remove-bulk-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoilaNorbert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/remove-bulk-file?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/remove-bulk-file?${params}`, {
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
| `id` | number | yes | The bulk file id to remove. |
| `recursive` | boolean | no | When true, remove related lists and contacts too. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recursive": true,
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recursive` | boolean |  |
| `result` | string |  |

## Native endpoint

Through the native VoilaNorbert API, this operation is `DELETE /massives/:id` (base URL `https://api.voilanorbert.com/2018-01-08`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-bulk-file.md) for the provider-specific parameters and requirements.

