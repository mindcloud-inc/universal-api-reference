# ImageKit.io: Remove Tags Bulk

Removes tags from multiple files in ImageKit.io.

```
PUT https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/remove-tags-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageKit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/remove-tags-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/remove-tags-bulk', {
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
| `fileIds` | list<string> | no | Default: `["6995e3df5c7cd75eb84cddae"]`. |
| `tags` | list<string> | no | Default: `["codex-tag"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "successfullyUpdatedFileIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `successfullyUpdatedFileIds` | array<string> |  |

## Native endpoint

Through the native ImageKit.io API, this operation is `POST /files/removeTags` (base URL `https://api.imagekit.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tags-bulk.md) for the provider-specific parameters and requirements.

