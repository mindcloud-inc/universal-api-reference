# Documint: Delete Template

Permanently deletes an existing template from Documint.

```
DELETE https://connect.mindcloud.co/v1/universal/documint/latest/actions/delete-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/documint/latest/actions/delete-template?connectionId=$CONNECTION_ID&id=69bac297724eda8b0297192e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "69bac297724eda8b0297192e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documint/latest/actions/delete-template?${params}`, {
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
| `id` | string | yes | The Documint template ID to delete. Example: `69bac297724eda8b0297192e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assets": [
        "string"
      ],
      "components": {},
      "id": "string",
      "name": "Ava Chen",
      "options": {},
      "thumbnail": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assets` | array<string> |  |
| `components` | object |  |
| `id` | string |  |
| `name` | string |  |
| `options` | object |  |
| `thumbnail` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Documint API, this operation is `DELETE /templates/:id` (base URL `https://api.documint.me/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template.md) for the provider-specific parameters and requirements.

