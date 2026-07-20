# ScrapingDog: Search Google Hotels

Retrieves Google Hotels search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-hotels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-hotels?connectionId=$CONNECTION_ID&checkInDate=string&checkOutDate=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "checkInDate": "string",
  "checkOutDate": "string",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-hotels?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checkInDate` | string | yes | Check-in date in YYYY-MM-DD format. |
| `checkOutDate` | string | yes | Check-out date in YYYY-MM-DD format. |
| `query` | string | yes | Search query for Google Hotels. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": [
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
| `ads` | array<object> |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_hotels` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-hotels.md) for the provider-specific parameters and requirements.

