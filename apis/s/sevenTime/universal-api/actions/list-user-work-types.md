# Seven Time: List User Work Types

Retrieves user work types from Seven Time.

```
GET https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-user-work-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven Time `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-user-work-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-user-work-types?${params}`, {
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
      "Id": "string",
      "name": "Ava Chen",
      "pricePerHour": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | string |  |
| `name` | string |  |
| `pricePerHour` | number |  |

## Native endpoint

Through the native Seven Time API, this operation is `GET /userWorkTypes` (base URL `https://app.seventime.se/api/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-work-types.md) for the provider-specific parameters and requirements.

