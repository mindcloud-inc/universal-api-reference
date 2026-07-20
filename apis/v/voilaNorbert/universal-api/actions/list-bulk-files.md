# VoilaNorbert: List Bulk Files

Retrieves bulk files from VoilaNorbert in chronological order.

```
GET https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/list-bulk-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoilaNorbert `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/list-bulk-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/list-bulk-files?${params}`, {
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
      "result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | array<object> |  |

## Native endpoint

Through the native VoilaNorbert API, this operation is `GET /massives/` (base URL `https://api.voilanorbert.com/2018-01-08`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bulk-files.md) for the provider-specific parameters and requirements.

