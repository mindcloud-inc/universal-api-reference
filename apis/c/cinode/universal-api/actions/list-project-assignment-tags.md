# Cinode: List Project Assignment Tags

Retrieves tags for a project assignment in Cinode.

```
GET https://connect.mindcloud.co/v1/universal/cinode/latest/actions/list-project-assignment-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cinode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cinode/latest/actions/list-project-assignment-tags?connectionId=$CONNECTION_ID&companyId=1&projectId=1&roleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1",
  "projectId": "1",
  "roleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cinode/latest/actions/list-project-assignment-tags?${params}`, {
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
| `companyId` | number | yes | Cinode company identifier. |
| `projectId` | number | yes | Identifier of the project. |
| `roleId` | number | yes | Identifier of the project assignment role. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "id": 1,
      "name": "Ava Chen",
      "seoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `id` | number |  |
| `name` | string |  |
| `seoId` | string |  |

## Native endpoint

Through the native Cinode API, this operation is `GET /v0.2/companies/:companyId/projects/:projectId/roles/:roleId/tags` (base URL `https://api.cinode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-assignment-tags.md) for the provider-specific parameters and requirements.

