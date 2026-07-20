# Zeplin: List Organization Member Projects

Retrieves a list of organization member projects from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-organization-member-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-organization-member-projects?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string&memberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string",
  "memberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-organization-member-projects?${params}`, {
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
| `memberId` | string | yes | Member id |

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
      "number_of_text_styles": 1,
      "platform": "string",
      "scene_url": "https://example.com",
      "status": "string",
      "thumbnail": "string",
      "updated": 1
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
| `number_of_text_styles` | number |  |
| `platform` | string |  |
| `scene_url` | string |  |
| `status` | string |  |
| `thumbnail` | string |  |
| `updated` | number |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /organizations/{organization_id}/members/{member_id}/projects` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organization-member-projects.md) for the provider-specific parameters and requirements.

