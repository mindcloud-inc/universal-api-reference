# Storydoc: Create Story Version

Creates a new story version in Storydoc.

```
POST https://connect.mindcloud.co/v1/universal/storydoc/latest/actions/create-story-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storydoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/storydoc/latest/actions/create-story-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storyId": "string",
  "senderEmail": "ava@example.com",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storydoc/latest/actions/create-story-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "storyId": "string",
    "senderEmail": "ava@example.com",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `storyId` | string | yes | The ID of the story template to version. |
| `senderEmail` | string | yes | Email of the sender. It must exist in the Storydoc organization. |
| `daysToExpire` | number | no | Number of days until the version expires. |
| `data` | object | yes | Storydoc version data object. It must include at least a title field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "editorUrl": "https://example.com",
      "shortUrl": "https://example.com",
      "url": "https://example.com",
      "versionId": "string",
      "versionUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `editorUrl` | string | Storydoc editor URL for the created version. |
| `shortUrl` | string | Shortened public URL for the created version. |
| `url` | string | Public URL for the created version. |
| `versionId` | string | Unique identifier for the created version. |
| `versionUrl` | string | Storydoc version details URL. |

## Native endpoint

Through the native Storydoc API, this operation is `POST /v2/versions` (base URL `https://api.storydoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-story-version.md) for the provider-specific parameters and requirements.

