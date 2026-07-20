# Cinode: Add Project Assignment Tag

Adds a tag to a project assignment in Cinode.

```
POST https://connect.mindcloud.co/v1/universal/cinode/latest/actions/add-project-assignment-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cinode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cinode/latest/actions/add-project-assignment-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "projectId": 1,
  "roleId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cinode/latest/actions/add-project-assignment-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "projectId": 1,
    "roleId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Cinode company identifier. |
| `projectId` | number | yes | Identifier of the project. |
| `roleId` | number | yes | Identifier of the project assignment role. |
| `id` | number | no | Existing tag identifier to add. |
| `name` | string | no | Tag name to create or match. |

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

Through the native Cinode API, this operation is `POST /v0.2/companies/:companyId/projects/:projectId/roles/:roleId/tags` (base URL `https://api.cinode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-project-assignment-tag.md) for the provider-specific parameters and requirements.

