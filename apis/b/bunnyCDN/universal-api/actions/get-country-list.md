# BunnyCDN: Get Country List

Retrieves the country list from BunnyCDN.

```
GET https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-country-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-country-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-country-list?${params}`, {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | List of countries and tax-rate entries. |

## Native endpoint

Through the native BunnyCDN API, this operation is `GET /country` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-country-list.md) for the provider-specific parameters and requirements.

