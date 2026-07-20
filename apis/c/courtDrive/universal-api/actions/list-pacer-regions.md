# Court Drive: List PACER Regions



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/list-pacer-regions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/list-pacer-regions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/list-pacer-regions?${params}`, {
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
      "regions": [
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
| `regions` | array<object> |  |

## Native endpoint

Through the native Court Drive API, this operation is `GET /regions/pacer` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pacer-regions.md) for the provider-specific parameters and requirements.

