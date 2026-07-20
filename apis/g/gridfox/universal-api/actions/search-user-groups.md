# Gridfox: Search User Groups

Finds user groups in a Gridfox project.

```
GET https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/search-user-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gridfox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/search-user-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/search-user-groups?${params}`, {
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
      "data": [
        {}
      ],
      "pageNumber": 1,
      "pageSize": 1,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | User groups returned by the project search. |
| `pageNumber` | number | Current page number. |
| `pageSize` | number | Page size used by the response. |
| `totalPages` | number | Total number of pages. |
| `totalRecords` | number | Total number of matching groups. |

## Native endpoint

Through the native Gridfox API, this operation is `GET /groups` (base URL `https://api.gridfox.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-user-groups.md) for the provider-specific parameters and requirements.

