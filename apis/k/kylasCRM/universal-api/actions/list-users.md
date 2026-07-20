# Kylas CRM: List Users



```
GET https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kylas CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/list-users?${params}`, {
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
      "content": [
        "string"
      ],
      "first": true,
      "last": true,
      "number": 1,
      "numberOfElements": 1,
      "size": 1,
      "sort": [
        "string"
      ],
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | array | Page of user records. |
| `first` | boolean | Whether this is the first page. |
| `last` | boolean | Whether this is the last page. |
| `number` | number | Current page number. |
| `numberOfElements` | number | Number of users returned in this page. |
| `size` | number | Page size. |
| `sort` | array | Sort metadata for the page. |
| `totalElements` | number | Total number of matching users. |
| `totalPages` | number | Total number of pages available. |

## Native endpoint

Through the native Kylas CRM API, this operation is `GET /users` (base URL `https://api.kylas.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

