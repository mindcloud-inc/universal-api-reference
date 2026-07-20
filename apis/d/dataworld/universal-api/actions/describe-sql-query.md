# data.world: Describe a SQL Query

Describes a SQL query in data.world.

```
GET https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/describe-sql-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a data.world `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/describe-sql-query?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/describe-sql-query?${params}`, {
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
      "fields": [
        {
          "name": "Ava Chen",
          "type": "string"
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
| `fields[].name` | string |  |
| `fields[].type` | string |  |

## Native endpoint

Through the native data.world API, this operation is `POST /sql/{owner}/{id}/describe` (base URL `https://api.data.world/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/describe-sql-query.md) for the provider-specific parameters and requirements.

