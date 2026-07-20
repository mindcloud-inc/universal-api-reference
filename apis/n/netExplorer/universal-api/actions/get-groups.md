# NetExplorer: List Groups



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-groups?${params}`, {
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
      "nbObjets": 1,
      "nbTotalObjects": 1,
      "objects": [
        {
          "id": 1,
          "login": "string"
        }
      ],
      "offsetStart": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nbObjets` | number |  |
| `nbTotalObjects` | number |  |
| `objects` | array<object> |  |
| `objects[].id` | number |  |
| `objects[].login` | string |  |
| `offsetStart` | number |  |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /groups` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-groups.md) for the provider-specific parameters and requirements.

