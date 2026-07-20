# ClassDo: List Organization Members

Retrieves organization member records from ClassDo.

```
GET https://connect.mindcloud.co/v1/universal/classDo/latest/actions/list-organization-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassDo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classDo/latest/actions/list-organization-members?connectionId=$CONNECTION_ID&query=query%20ListOrganizationMembers%20%7B%20viewer%20%7B%20members(input%3A%20%7B%20first%3A%2050%20%7D)%20%7B%20totalCount%20edges%20%7B%20node%20%7B%20id%20%7D%20%7D%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query ListOrganizationMembers { viewer { members(input: { first: 50 }) { totalCount edges { node { id } } } } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classDo/latest/actions/list-organization-members?${params}`, {
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
| `query` | string | yes | GraphQL query payload. Default: `query ListOrganizationMembers { viewer { members(input: { first: 50 }) { totalCount edges { node { id } } } } }`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "viewer": {
          "members": {
            "edges": [
              {
                "node": {
                  "id": "string"
                }
              }
            ],
            "totalCount": 1
          }
        }
      },
      "errors": [
        {
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
| `data.viewer.members.edges[].node.id` | string |  |
| `data.viewer.members.totalCount` | number |  |
| `errors[].message` | string |  |

## Native endpoint

Through the native ClassDo API, this operation is `POST /graphql` (base URL `https://api.classdo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-members.md) for the provider-specific parameters and requirements.

