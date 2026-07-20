# Linkly: Delete Link

Deletes an existing link from Linkly.

```
DELETE https://connect.mindcloud.co/v1/universal/linkly/latest/actions/delete-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/linkly/latest/actions/delete-link?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkly/latest/actions/delete-link?${params}`, {
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
| `id` | number | yes | The id of the Link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Delete confirmation message. |

## Native endpoint

Through the native Linkly API, this operation is `DELETE /workspace/:workspace_id/links/:id` (base URL `https://app.linklyhq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-link.md) for the provider-specific parameters and requirements.

