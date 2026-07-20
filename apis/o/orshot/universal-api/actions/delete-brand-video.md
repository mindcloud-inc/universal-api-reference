# Orshot: Delete Brand Video



```
DELETE https://connect.mindcloud.co/v1/universal/orshot/latest/actions/delete-brand-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orshot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/delete-brand-video?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orshot/latest/actions/delete-brand-video?${params}`, {
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
| `id` | string | yes | The brand video ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Identifier of the deleted video asset. |
| `message` | string | Deletion result message returned by Orshot. |

## Native endpoint

Through the native Orshot API, this operation is `DELETE /brand-assets/videos/delete/:id` (base URL `https://api.orshot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-brand-video.md) for the provider-specific parameters and requirements.

