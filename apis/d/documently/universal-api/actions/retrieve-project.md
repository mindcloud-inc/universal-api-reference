# Documently: Retrieve Project

Retrieves a project from Documently.

```
GET https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-project?${params}`, {
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
| `projectId` | string | no | The project id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "defaultLanguage": "string",
      "hash": "string",
      "id": "string",
      "languages": [
        "string"
      ],
      "metadata": {},
      "name": "Ava Chen",
      "organization": "string",
      "publicUrl": true,
      "roles": [
        "string"
      ],
      "sortOrder": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `@type` | string |  |
| `defaultLanguage` | string |  |
| `hash` | string |  |
| `id` | string |  |
| `languages` | array<string> |  |
| `metadata` | object |  |
| `name` | string |  |
| `organization` | string |  |
| `publicUrl` | boolean |  |
| `roles` | array<string> |  |
| `sortOrder` | array<string> |  |

## Native endpoint

Through the native Documently API, this operation is `GET /projects/:projectId` (base URL `https://app.documently.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-project.md) for the provider-specific parameters and requirements.

