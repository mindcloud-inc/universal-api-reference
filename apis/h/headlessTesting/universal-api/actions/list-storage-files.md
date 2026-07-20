# Headless Testing: List Storage Files

Retrieves storage files from Headless Testing.

```
GET https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/list-storage-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/list-storage-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/list-storage-files?${params}`, {
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
      "items": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Headless Testing API, this operation is `GET /storage` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-storage-files.md) for the provider-specific parameters and requirements.

