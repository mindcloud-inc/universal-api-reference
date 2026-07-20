# Kazm: List File Sets

Retrieves file sets from Kazm.

```
GET https://connect.mindcloud.co/v1/universal/kazm/latest/actions/list-file-sets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kazm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kazm/latest/actions/list-file-sets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kazm/latest/actions/list-file-sets?${params}`, {
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
      "file_sets": [
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
| `file_sets` | array<object> |  |

## Native endpoint

Through the native Kazm API, this operation is `GET /filesets` (base URL `https://api.lightningrod.ai/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-file-sets.md) for the provider-specific parameters and requirements.

