# Agentset: Create Batch Upload URLs

Creates presigned batch file upload URLs in Agentset.

```
POST https://connect.mindcloud.co/v1/universal/agentset/latest/actions/create-batch-upload-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agentset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentset/latest/actions/create-batch-upload-urls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files[]": [
    {}
  ],
  "namespaceId": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentset/latest/actions/create-batch-upload-urls', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files[]": [{}],
    "namespaceId": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files[]` | array<object> | yes | The files to create upload URLs for. |
| `namespaceId` | string | yes | The Agentset namespace ID, prefixed with ns_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "key": "string",
        "url": "https://example.com"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data.key` | string |  |
| `data.url` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Agentset API, this operation is `POST /v1/namespace/:namespaceId/uploads/batch` (base URL `https://api.agentset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch-upload-urls.md) for the provider-specific parameters and requirements.

