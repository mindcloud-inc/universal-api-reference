# SeaTable: List Row Activities

Lists row activities in a SeaTable base.

```
GET https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/list-row-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/list-row-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/list-row-activities?${params}`, {
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
      "activities": [
        {}
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities` | array<object> |  |
| `totalCount` | number |  |

## Native endpoint

Through the native SeaTable API, this operation is `GET /api-gateway/api/v2/dtables/:base_uuid/activities/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-row-activities.md) for the provider-specific parameters and requirements.

