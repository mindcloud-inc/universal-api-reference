# Localazy: List Projects

Retrieves projects from Localazy.

```
GET https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-projects?${params}`, {
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
| `organization` | boolean | no | Include organization feature and quota information in the response. |
| `languages` | boolean | no | Include languages and translation counts in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "image": "string",
      "languages": [
        {}
      ],
      "name": "Ava Chen",
      "organization": {},
      "orgId": "string",
      "role": "string",
      "slug": "string",
      "sourceLanguage": 1,
      "tone": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Project description. |
| `id` | string | Unique project identifier. |
| `image` | string | Project image URL. |
| `languages` | array<object> | Project languages and translation counts. |
| `name` | string | Project name. |
| `organization` | object | Organization-level feature flags and quotas. |
| `orgId` | string | Identifier of the organization that owns the project. |
| `role` | string | Role of the current token in the project. |
| `slug` | string | Project slug. |
| `sourceLanguage` | number | Source language identifier. |
| `tone` | string | Project tone. |
| `type` | string | Project type. |
| `url` | string | Project URL in Localazy. |

## Native endpoint

Through the native Localazy API, this operation is `GET /projects` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

