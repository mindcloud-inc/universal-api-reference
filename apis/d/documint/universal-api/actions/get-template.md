# Documint: Get Template

Retrieves a template from Documint by ID.

```
GET https://connect.mindcloud.co/v1/universal/documint/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documint/latest/actions/get-template?connectionId=$CONNECTION_ID&id=69bac297724eda8b0297192e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "69bac297724eda8b0297192e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documint/latest/actions/get-template?${params}`, {
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
| `id` | string | yes | The Documint template ID. Example: `69bac297724eda8b0297192e`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated list of fields to include in the returned template. Example: `name,thumbnail`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "options": {},
      "tags": [
        "string"
      ],
      "testData": {},
      "thumbnail": {},
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Template creation timestamp. |
| `id` | string | Template ID. |
| `name` | string | Template name. |
| `options` | object | Template document options. |
| `tags` | array<string> | Template tags. |
| `testData` | object | Template sample merge data. |
| `thumbnail` | object | Template thumbnail metadata. |
| `type` | string | Template type. |
| `updatedAt` | string | Template update timestamp. |

## Native endpoint

Through the native Documint API, this operation is `GET /templates/:id` (base URL `https://api.documint.me/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

