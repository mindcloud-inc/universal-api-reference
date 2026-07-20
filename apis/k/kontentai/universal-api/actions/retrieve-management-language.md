# Kontent.ai: Retrieve management language

Retrieves a language from your Kontent.ai environment.

```
GET https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-management-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-management-language?connectionId=$CONNECTION_ID&languageIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "languageIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-management-language?${params}`, {
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
| `languageIdentifier` | string | yes | Kontent.ai language identifier. |

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

Through the native Kontent.ai API, this operation is `GET https://manage.kontent.ai/v2/projects/:environment_id/languages/:language_identifier` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-management-language.md) for the provider-specific parameters and requirements.

