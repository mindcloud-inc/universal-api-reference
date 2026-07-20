# Google Ads: List Customer Manager Links

Retrieves customer manager links from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-manager-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-manager-links?connectionId=$CONNECTION_ID&customerId=1234567890&query=SELECT%20customer_manager_link.manager_customer%2C%20customer_manager_link.status%20FROM%20customer_manager_link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "query": "SELECT customer_manager_link.manager_customer, customer_manager_link.status FROM customer_manager_link"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-manager-links?${params}`, {
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
| `customerId` | list<string> | yes | Customer ID to query (without dashes). Example: `1234567890`. |
| `query` | string | yes | GAQL query for customer_manager_link visibility. Default: `SELECT customer_manager_link.manager_customer, customer_manager_link.resource_name, customer_manager_link.status FROM customer_manager_link`. Example: `SELECT customer_manager_link.manager_customer, customer_manager_link.status FROM customer_manager_link`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerManagerLink": {
        "managerCustomer": "https://example.com",
        "resourceName": "https://example.com",
        "status": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerManagerLink.managerCustomer` | string |  |
| `customerManagerLink.resourceName` | string |  |
| `customerManagerLink.status` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-manager-links.md) for the provider-specific parameters and requirements.

