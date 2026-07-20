# PromptLayer Run Agent: Get Skill Collection

Retrieves a PromptLayer skill collection.

```
GET https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-skill-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-skill-collection?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-skill-collection?${params}`, {
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
| `identifier` | string | yes | Skill collection UUID, name, or root path. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | list | no | Optional response format. Use zip for an archive download. |
| `label` | string | no | Release label for the version to fetch. |
| `version` | number | no | Specific version number to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "files": {},
      "skillCollection": {},
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
| `files` | object |  |
| `skillCollection` | object |  |
| `success` | boolean |  |
| `version` | object |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `GET /api/public/v2/skill-collections/:identifier` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-skill-collection.md) for the provider-specific parameters and requirements.

