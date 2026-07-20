# Nautical: List Permission Groups

Retrieves a list of permission groups from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-permission-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-permission-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-permission-groups?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "permissionGroups": {
          "edges": [
            {
              "node": {
                "id": "string",
                "name": "Ava Chen",
                "userCanManage": true
              }
            }
          ],
          "pageInfo": {
            "endCursor": "string",
            "hasNextPage": true
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.permissionGroups.edges[].node.id` | string |  |
| `data.permissionGroups.edges[].node.name` | string |  |
| `data.permissionGroups.edges[].node.userCanManage` | boolean |  |
| `data.permissionGroups.pageInfo.endCursor` | string |  |
| `data.permissionGroups.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-permission-groups.md) for the provider-specific parameters and requirements.

