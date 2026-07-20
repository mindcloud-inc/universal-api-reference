# Redbooth: Get Project

Retrieves a project from Redbooth.

```
GET https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Redbooth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/get-project?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/get-project?${params}`, {
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
| `id` | number | yes | Redbooth project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "created_at": 1,
      "deleted": true,
      "id": 1,
      "name": "Ava Chen",
      "organization_id": 1,
      "permalink": "https://example.com",
      "public": true,
      "publish_pages": true,
      "tracks_time": true,
      "type": "string",
      "updated_at": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `created_at` | number |  |
| `deleted` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `organization_id` | number |  |
| `permalink` | string |  |
| `public` | boolean |  |
| `publish_pages` | boolean |  |
| `tracks_time` | boolean |  |
| `type` | string |  |
| `updated_at` | number |  |
| `user_id` | number |  |

## Native endpoint

Through the native Redbooth API, this operation is `GET /projects/:id` (base URL `https://redbooth.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

