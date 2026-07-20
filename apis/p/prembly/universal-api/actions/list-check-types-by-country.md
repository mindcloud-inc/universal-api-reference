# Prembly: List Check Types by Country

Retrieves check types by country from Prembly.

```
GET https://connect.mindcloud.co/v1/universal/prembly/latest/actions/list-check-types-by-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/list-check-types-by-country?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prembly/latest/actions/list-check-types-by-country?${params}`, {
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
      "cost": 1,
      "country": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "turnaround_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | number |  |
| `country` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `turnaround_time` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `GET /api/v1/api/bgc/country/check-types/` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-check-types-by-country.md) for the provider-specific parameters and requirements.

