# Localazy: Update Screenshot Metadata

Updates screenshot tags, phrases, or metadata in Localazy.

```
PUT https://connect.mindcloud.co/v1/universal/localazy/latest/actions/update-screenshot-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/update-screenshot-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "screenshotId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/localazy/latest/actions/update-screenshot-metadata', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "screenshotId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Localazy project identifier or slug. |
| `screenshotId` | string | yes | Identifier of the screenshot to update. |
| `comment` | string | no | Custom screenshot description. |
| `addTags[]` | array<string> | no | Tags to add to the screenshot. |
| `removeTags[]` | array<string> | no | Tags to remove from the screenshot. |
| `tags[]` | array<string> | no | Replacement tag list for the screenshot. |
| `addPhrases[]` | array<string> | no | Phrase identifiers to add to the screenshot. |
| `removePhrases[]` | array<string> | no | Phrase identifiers to remove from the screenshot. |
| `phrases[]` | array<string> | no | Replacement phrase identifier list for the screenshot. |
| `addMetadata` | object | no | Metadata entries to add. |
| `removeMetadata[]` | array<string> | no | Metadata keys to remove. |
| `metadata` | object | no | Replacement metadata object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean | Whether the screenshot metadata update succeeded. |

## Native endpoint

Through the native Localazy API, this operation is `PUT /projects/:projectId/screenshots/:screenshotId` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-screenshot-metadata.md) for the provider-specific parameters and requirements.

