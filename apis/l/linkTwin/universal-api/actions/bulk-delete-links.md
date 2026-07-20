# LinkTwin: Bulk Delete Links

Deletes multiple existing links from LinkTwin.

```
DELETE https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/bulk-delete-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/bulk-delete-links?connectionId=$CONNECTION_ID&ids%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/bulk-delete-links?${params}`, {
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
| `ids[]` | array<number> | yes | Link IDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": [
        1
      ],
      "error": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted[]` | number |  |
| `error` | number |  |

## Native endpoint

Through the native LinkTwin API, this operation is `POST /urls/delete` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-delete-links.md) for the provider-specific parameters and requirements.

