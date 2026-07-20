# LinkedIn Ads Reports: Search Ad Accounts

Finds ad accounts in LinkedIn Ads Reports.

```
GET https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/search-ad-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn Ads Reports `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/search-ad-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/search-ad-accounts?${params}`, {
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
      "currency": "string",
      "id": "string",
      "name": "Ava Chen",
      "reference": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `id` | string |  |
| `name` | string |  |
| `reference` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native LinkedIn Ads Reports API, this operation is `GET /rest/adAccounts` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-ad-accounts.md) for the provider-specific parameters and requirements.

