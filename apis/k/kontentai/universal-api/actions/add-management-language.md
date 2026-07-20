# Kontent.ai: Add management language

Creates a new language in Kontent.ai.

```
POST https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/add-management-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/add-management-language" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/add-management-language', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | JSON request body for creating a Kontent.ai language. |

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

Through the native Kontent.ai API, this operation is `POST https://manage.kontent.ai/v2/projects/:environment_id/languages` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-management-language.md) for the provider-specific parameters and requirements.

