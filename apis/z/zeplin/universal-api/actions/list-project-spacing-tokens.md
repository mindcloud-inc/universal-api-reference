# Zeplin: List Project Spacing Tokens

Retrieves a list of project spacing tokens from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-project-spacing-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-project-spacing-tokens?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-project-spacing-tokens?${params}`, {
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
| `projectId` | string | yes | Project id |
| `includeLinkedStyleguides` | boolean | no | Whether to include linked styleguides or not |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": {},
      "id": "string",
      "name": "Ava Chen",
      "section": {},
      "source": {},
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | object |  |
| `id` | string |  |
| `name` | string |  |
| `section` | object |  |
| `source` | object |  |
| `value` | number |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /projects/{project_id}/spacing_tokens` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-spacing-tokens.md) for the provider-specific parameters and requirements.

