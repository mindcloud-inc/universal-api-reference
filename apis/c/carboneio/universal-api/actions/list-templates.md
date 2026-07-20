# Carbone.io: List Templates

Retrieves templates from Carbone.io.

```
GET https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbone.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/list-templates?${params}`, {
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
| `category` | string | no | Filter results to templates in one category. |
| `id` | string | no | Filter results to one Carbone template ID. |
| `includeVersions` | boolean | no | Include all versions for a specific template ID. |
| `origin` | number | no | Filter by template upload origin: 0 for API uploads or 1 for Studio uploads. |
| `search` | string | no | Search template names, template IDs, or version IDs. |
| `versionId` | string | no | Filter results to one template version ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "comment": "string",
      "createdAt": 1,
      "deployedAt": 1,
      "expireAt": 1,
      "id": "string",
      "name": "Ava Chen",
      "origin": 1,
      "size": 1,
      "tags": [
        "string"
      ],
      "type": "string",
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Template category. |
| `comment` | string | Template comment. |
| `createdAt` | number | UTC Unix timestamp when the version was created. |
| `deployedAt` | number | UTC Unix timestamp of the deployed version. |
| `expireAt` | number | UTC Unix timestamp when the version expires. |
| `id` | string | Template ID. |
| `name` | string | Template name. |
| `origin` | number | Upload origin: 0 API, 1 Studio. |
| `size` | number | Template file size in bytes. |
| `tags` | array<string> | Template tags. |
| `type` | string | Template file type. |
| `versionId` | string | Version ID for the specific template revision. |

## Native endpoint

Through the native Carbone.io API, this operation is `GET /templates` (base URL `https://api.carbone.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

