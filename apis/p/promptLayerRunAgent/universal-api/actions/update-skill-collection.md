# PromptLayer Run Agent: Update Skill Collection

Updates an existing skill collection in PromptLayer.

```
PUT https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/update-skill-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/update-skill-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/update-skill-collection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | Skill collection UUID, name, or root path. |
| `name` | string | yes | Updated name for the skill collection. |

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

Through the native PromptLayer Run Agent API, this operation is `PATCH /api/public/v2/skill-collections/:identifier` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-skill-collection.md) for the provider-specific parameters and requirements.

