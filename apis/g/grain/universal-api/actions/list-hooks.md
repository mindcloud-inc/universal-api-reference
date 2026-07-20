# Grain: List Hooks

Retrieves hooks from Grain.

```
GET https://connect.mindcloud.co/v1/universal/grain/latest/actions/list-hooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grain/latest/actions/list-hooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grain/latest/actions/list-hooks?${params}`, {
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
| `filter` | object | no |  |
| `filter.hook_type` | list | no | Only return hooks with the matching hook type. One of: `highlight_added`, `highlight_deleted`, `highlight_updated`, `recording_added`, `recording_deleted`, `recording_updated`, `story_added`, `story_deleted`, `story_updated`, `upload_status`. |
| `filter.state` | list | no | Only return hooks that are either enabled or disabled. One of: `disabled`, `enabled`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "hookType": "string",
      "hookUrl": "https://example.com",
      "id": "string",
      "include": {},
      "insertedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `hookType` | string |  |
| `hookUrl` | string |  |
| `id` | string |  |
| `include` | object |  |
| `insertedAt` | date |  |

## Native endpoint

Through the native Grain API, this operation is `POST /v2/hooks` (base URL `https://api.grain.com/_/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-hooks.md) for the provider-specific parameters and requirements.

