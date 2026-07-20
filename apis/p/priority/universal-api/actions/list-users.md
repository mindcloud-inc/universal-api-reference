# Priority: List Users

Retrieves users from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/list-users?${params}`, {
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
      "GROUPNAME": "Ava Chen",
      "SNAME": "Ava Chen",
      "USERID": 1,
      "USERLOGIN": "string",
      "USERNAME": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `GROUPNAME` | string |  |
| `SNAME` | string |  |
| `USERID` | number |  |
| `USERLOGIN` | string |  |
| `USERNAME` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /USERS` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

