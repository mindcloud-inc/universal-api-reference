# PromptLayer Run Agent: Save Skill Collection Version

Creates a new PromptLayer skill collection version.

```
POST https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/save-skill-collection-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/save-skill-collection-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/save-skill-collection-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | Skill collection UUID, name, or root path. |
| `file_updates[]` | array<object> | no | Inline file additions or replacements for the new version. Example: `[object Object]`. |
| `commitMessage` | string | no | Optional commit message for the saved version. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `moves[]` | array<object> | no | File move operations for the new version. |
| `deletes[]` | array<string> | no | File paths to delete in the new version. |
| `releaseLabel` | string | no | Optional release label to assign to the new version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "version": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `version` | object |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /api/public/v2/skill-collections/:identifier/versions` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-skill-collection-version.md) for the provider-specific parameters and requirements.

