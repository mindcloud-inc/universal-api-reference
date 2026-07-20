# Rebrandly: Delete Tag

Deletes an existing tag from Rebrandly.

```
DELETE https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/delete-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/delete-tag?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/delete-tag?${params}`, {
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
| `id` | string | yes | Unique identifier of the tag to permanently delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "color": "string",
      "deleted": true,
      "id": "string",
      "name": "Ava Chen",
      "scans": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number |  |
| `color` | string |  |
| `deleted` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `scans` | object |  |

## Native endpoint

Through the native Rebrandly API, this operation is `DELETE /tags/:id` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tag.md) for the provider-specific parameters and requirements.

