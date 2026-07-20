# Zeplin: List Organization Projects

Retrieves a list of organization projects from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-organization-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-organization-projects?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-organization-projects?${params}`, {
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
| `organizationId` | string | yes | Organization id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "description": "string",
      "id": "string",
      "linked_styleguide": {},
      "name": "Ava Chen",
      "number_of_colors": 1,
      "number_of_components": 1,
      "number_of_connected_components": 1,
      "number_of_members": 1,
      "number_of_screens": 1,
      "number_of_spacing_tokens": 1,
      "number_of_text_styles": 1,
      "organization": {},
      "platform": "string",
      "status": "string",
      "thumbnail": "string",
      "updated": 1,
      "workflow_status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `description` | string |  |
| `id` | string |  |
| `linked_styleguide` | object |  |
| `name` | string |  |
| `number_of_colors` | number |  |
| `number_of_components` | number |  |
| `number_of_connected_components` | number |  |
| `number_of_members` | number |  |
| `number_of_screens` | number |  |
| `number_of_spacing_tokens` | number |  |
| `number_of_text_styles` | number |  |
| `organization` | object |  |
| `platform` | string |  |
| `status` | string |  |
| `thumbnail` | string |  |
| `updated` | number |  |
| `workflow_status` | object |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /organizations/{organization_id}/projects` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organization-projects.md) for the provider-specific parameters and requirements.

