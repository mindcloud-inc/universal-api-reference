# Papersign: List Papersign Spaces



```
GET https://connect.mindcloud.co/v1/universal/papersign/latest/actions/list-papersign-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papersign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/papersign/latest/actions/list-papersign-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/papersign/latest/actions/list-papersign-spaces?${params}`, {
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
      "has_more": true,
      "limit": 1,
      "results": {
        "spaces": [
          {
            "allow_team_access": true,
            "id": 1,
            "name": "Ava Chen",
            "root_folder_id": 1
          }
        ]
      },
      "skip": 1,
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_more` | boolean | Whether more spaces are available. |
| `limit` | number | The page size used for the response. |
| `results.spaces[].allow_team_access` | boolean | Whether team access is allowed for the space. |
| `results.spaces[].id` | number | The unique identifier of the space. |
| `results.spaces[].name` | string | The name of the space. |
| `results.spaces[].root_folder_id` | number | The unique identifier of the root folder. |
| `skip` | number | The number of skipped records. |
| `status` | string | Response status. |
| `total` | number | The total number of spaces. |

## Native endpoint

Through the native Papersign API, this operation is `GET /papersign/spaces` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-papersign-spaces.md) for the provider-specific parameters and requirements.

