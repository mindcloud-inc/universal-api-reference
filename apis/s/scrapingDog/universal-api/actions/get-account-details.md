# ScrapingDog: Get Account Details

Retrieves account details from ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-account-details?${params}`, {
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
      "concurrencyLimit": 1,
      "email": "ava@example.com",
      "linkedinConcurrencyLimit": 1,
      "linkedinThreadCount": 1,
      "pack": "string",
      "packType": "string",
      "requestLimit": 1,
      "requestUsed": 1,
      "threadCount": 1,
      "username": "Ava Chen",
      "validity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `concurrencyLimit` | number | Maximum concurrent requests allowed on the account. |
| `email` | string | Account email returned by ScrapingDog. |
| `linkedinConcurrencyLimit` | number | Separate concurrency limit returned for LinkedIn-related requests. |
| `linkedinThreadCount` | number | Current LinkedIn thread count returned by the account endpoint. |
| `pack` | string | Current ScrapingDog plan name. |
| `packType` | string | Billing cadence or plan type for the current package. |
| `requestLimit` | number | Total request quota available for the current billing window. |
| `requestUsed` | number | Number of requests already consumed in the current billing window. |
| `threadCount` | number | Number of active threads currently in use. |
| `username` | string | Account username returned by ScrapingDog. |
| `validity` | number | Remaining validity value returned by the account endpoint. |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /account` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-details.md) for the provider-specific parameters and requirements.

