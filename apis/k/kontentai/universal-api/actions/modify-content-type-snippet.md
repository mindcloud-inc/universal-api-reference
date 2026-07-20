# Kontent.ai: Modify content type snippet

Modifies a content type snippet in Kontent.ai.

```
PUT https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/modify-content-type-snippet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/modify-content-type-snippet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "snippetIdentifier": "string",
  "operations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/modify-content-type-snippet', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "snippetIdentifier": "string",
    "operations[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `snippetIdentifier` | string | yes | Kontent.ai content type snippet identifier to modify. |
| `operations[]` | array<object> | yes | JSON Patch operations for modifying a Kontent.ai content type snippet. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codename": "Ava Chen",
      "elements": [
        {
          "codename": "Ava Chen",
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codename` | string | Content type snippet codename. |
| `elements[].codename` | string | Element codename. |
| `elements[].id` | string | Element ID. |
| `elements[].name` | string | Element name. |
| `id` | string | Content type snippet ID. |
| `name` | string | Content type snippet name. |

## Native endpoint

Through the native Kontent.ai API, this operation is `PATCH https://manage.kontent.ai/v2/projects/:environment_id/snippets/:snippet_identifier` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-content-type-snippet.md) for the provider-specific parameters and requirements.

