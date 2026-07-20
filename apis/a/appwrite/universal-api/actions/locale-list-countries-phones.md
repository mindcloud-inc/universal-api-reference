# Appwrite: List countries phone codes

Retrieves a list of countries phone codes from Appwrite.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/locale-list-countries-phones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/locale-list-countries-phones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/locale-list-countries-phones?${params}`, {
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
      "phones": [
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
| `phones` | array<object> | List of phones. |
| `total` | number | Total number of phones that matched your query. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /locale/countries/phones` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/locale-list-countries-phones.md) for the provider-specific parameters and requirements.

