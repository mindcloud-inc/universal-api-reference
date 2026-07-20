# Blaze AI: Delete Handbook Item

Deletes an existing handbook item from Blaze AI.

```
DELETE https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/delete-handbook-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/delete-handbook-item?connectionId=$CONNECTION_ID&workspace_id=994619&handbook_id=3412870&id=4979207" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace_id": "994619",
  "handbook_id": "3412870",
  "id": "4979207"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/delete-handbook-item?${params}`, {
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
| `workspace_id` | number | yes | Default: `994619`. |
| `handbook_id` | number | yes | Default: `3412870`. |
| `id` | number | yes | Default: `4979207`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `DELETE /api/v1/w/:workspace_id/handbooks/:handbook_id/items/:id` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-handbook-item.md) for the provider-specific parameters and requirements.

