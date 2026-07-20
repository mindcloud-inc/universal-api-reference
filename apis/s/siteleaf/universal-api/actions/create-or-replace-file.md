# Siteleaf: Create or Replace File

Creates or replaces a file in Siteleaf.

```
PUT https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/create-or-replace-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Siteleaf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/create-or-replace-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/create-or-replace-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | no | File attachment payload |
| `fileName` | string | no | Source file name or path |
| `siteId` | string | no | Siteleaf site identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "download_url": "https://example.com",
      "filesize": 1,
      "name": "Ava Chen",
      "sha": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `download_url` | string |  |
| `filesize` | number |  |
| `name` | string |  |
| `sha` | string |  |
| `type` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Siteleaf API, this operation is `PUT /sites/:site_id/source/:name` (base URL `https://api.siteleaf.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-replace-file.md) for the provider-specific parameters and requirements.

