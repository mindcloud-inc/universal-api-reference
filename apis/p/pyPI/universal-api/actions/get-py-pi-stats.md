# PyPI: Get PyPI Stats

Retrieves package size statistics from PyPI.

```
GET https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-py-pi-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PyPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-py-pi-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-py-pi-stats?${params}`, {
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
      "top_packages": {},
      "total_packages_size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `top_packages` | object | Top packages by size in bytes. |
| `total_packages_size` | number | Total size of packages served by PyPI. |

## Native endpoint

Through the native PyPI API, this operation is `GET /stats/` (base URL `https://pypi.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-py-pi-stats.md) for the provider-specific parameters and requirements.

