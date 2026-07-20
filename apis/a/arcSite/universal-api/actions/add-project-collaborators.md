# ArcSite: Add Project Collaborators

Adds collaborators to an existing ArcSite project.

```
PUT https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/add-project-collaborators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ArcSite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/add-project-collaborators" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "collaborators[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/arcSite/latest/actions/add-project-collaborators', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "collaborators[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The ID of the project. |
| `collaborators[]` | array<object> | yes | Collaborators to add to the project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failItems": [
        {
          "data": {
            "email": "ava@example.com",
            "role": "string"
          },
          "message": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failItems[].data.email` | string |  |
| `failItems[].data.role` | string |  |
| `failItems[].message` | string |  |

## Native endpoint

Through the native ArcSite API, this operation is `POST /projects/:projectId/add_collaborators` (base URL `https://api.arcsite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-project-collaborators.md) for the provider-specific parameters and requirements.

