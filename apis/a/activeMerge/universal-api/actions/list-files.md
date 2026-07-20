# ActiveMerge: List Files

Retrieves files and folders for the authenticated user from ActiveMerge.

```
GET https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveMerge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/list-files?${params}`, {
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
| `id` | number | no | Optional parent folder ID to list files from. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Files/folders list for the authenticated user. |

## Native endpoint

Through the native ActiveMerge API, this operation is `GET /api/files` (base URL `https://app.activemerge.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

