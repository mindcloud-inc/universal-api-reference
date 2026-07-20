# PromptLayer Run Agent: Create Skill Collection

Creates a new skill collection in PromptLayer.

```
POST https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-skill-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-skill-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "files[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-skill-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "files[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the skill collection. |
| `files[]` | array<object> | yes | Inline files to seed the skill collection. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | number | no | Optional folder ID that should contain the skill collection. |
| `provider` | string | no | Optional provider for the skill collection. Example: `openai`. |
| `commitMessage` | string | no | Optional commit message for the initial version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "skillCollection": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `skillCollection` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /api/public/v2/skill-collections` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-skill-collection.md) for the provider-specific parameters and requirements.

