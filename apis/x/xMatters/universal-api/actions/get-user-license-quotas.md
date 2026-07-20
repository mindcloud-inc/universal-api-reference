# xMatters: Get user license quotas

Retrieves user license quotas from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-user-license-quotas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-user-license-quotas?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-user-license-quotas?${params}`, {
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
      "fullUsers": {
        "active": 1,
        "total": 1,
        "unused": 1
      },
      "stakeholderUsers": {
        "active": 1,
        "total": 1,
        "unused": 1
      },
      "stakeholderUsersEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fullUsers.active` | number |  |
| `fullUsers.total` | number |  |
| `fullUsers.unused` | number |  |
| `stakeholderUsers.active` | number |  |
| `stakeholderUsers.total` | number |  |
| `stakeholderUsers.unused` | number |  |
| `stakeholderUsersEnabled` | boolean |  |

## Native endpoint

Through the native xMatters API, this operation is `GET people/license-quotas` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-user-license-quotas.md) for the provider-specific parameters and requirements.

