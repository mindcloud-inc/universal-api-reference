# Google Ads: List Accessible Customers



```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-accessible-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-accessible-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-accessible-customers?${params}`, {
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
      "id": "string",
      "resourceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Customer ID parsed from the Google Ads customer resource name. |
| `resourceName` | string | Google Ads customer resource name returned by ListAccessibleCustomers. |

## Native endpoint

Through the native Google Ads API, this operation is `GET v22/customers:listAccessibleCustomers` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accessible-customers.md) for the provider-specific parameters and requirements.

