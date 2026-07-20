# Zaia: Delete Tag

Deletes an existing tag from Zaia.

```
DELETE https://connect.mindcloud.co/v1/universal/zaia/latest/actions/delete-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zaia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zaia/latest/actions/delete-tag?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zaia/latest/actions/delete-tag?${params}`, {
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
| `id` | string | yes | The UUID of the tag to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Deletion result message. |

## Native endpoint

Through the native Zaia API, this operation is `DELETE /api/v1/tags/:id` (base URL `https://api.endless.zaia.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tag.md) for the provider-specific parameters and requirements.

