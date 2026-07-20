# Chat Aid: Upload Custom Sources

Uploads new custom sources to Chat Aid.

```
POST https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/upload-custom-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chat Aid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/upload-custom-sources" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/upload-custom-sources', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files` | file | yes | File to upload as a custom source. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | no | Team ID for the uploaded source. Defaults to organization-wide when omitted. Example: `team123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Chat Aid API, this operation is `POST /external/sources/custom` (base URL `https://api.chataid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-custom-sources.md) for the provider-specific parameters and requirements.

