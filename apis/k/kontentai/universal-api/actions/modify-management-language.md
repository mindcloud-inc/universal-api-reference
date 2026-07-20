# Kontent.ai: Modify management language

Modifies a language in your Kontent.ai environment.

```
PUT https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/modify-management-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/modify-management-language" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "languageIdentifier": "string",
  "operations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/modify-management-language', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "languageIdentifier": "string",
    "operations[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageIdentifier` | string | yes | Kontent.ai language identifier to modify. |
| `operations[]` | array<object> | yes | JSON Patch operations for modifying a Kontent.ai language. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codename": "Ava Chen",
      "id": "string",
      "is_default": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codename` | string | Language codename. |
| `id` | string | Language ID. |
| `is_default` | boolean | Whether this is the default language. |
| `name` | string | Language name. |

## Native endpoint

Through the native Kontent.ai API, this operation is `PATCH https://manage.kontent.ai/v2/projects/:environment_id/languages/:language_identifier` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-management-language.md) for the provider-specific parameters and requirements.

