# Google Ads: List Customer Client Hierarchy

Retrieves customer client hierarchy from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-client-hierarchy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-client-hierarchy?connectionId=$CONNECTION_ID&customerId=1234567890&query=SELECT%20customer_client.client_customer%2C%20customer_client.descriptive_name%20FROM%20customer_client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "query": "SELECT customer_client.client_customer, customer_client.descriptive_name FROM customer_client"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-client-hierarchy?${params}`, {
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
| `query` | string | yes | GAQL query for customer_client hierarchy. Default: `SELECT customer_client.client_customer, customer_client.descriptive_name, customer_client.level, customer_client.manager, customer_client.currency_code, customer_client.time_zone, customer_client.status FROM customer_client ORDER BY customer_client.level, customer_client.descriptive_name`. Example: `SELECT customer_client.client_customer, customer_client.descriptive_name FROM customer_client`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerClient": {
        "clientCustomer": "string",
        "currencyCode": "string",
        "descriptiveName": "Ava Chen",
        "level": "string",
        "manager": true,
        "resourceName": "Ava Chen",
        "status": "string",
        "timeZone": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerClient.clientCustomer` | string |  |
| `customerClient.currencyCode` | string |  |
| `customerClient.descriptiveName` | string |  |
| `customerClient.level` | string |  |
| `customerClient.manager` | boolean |  |
| `customerClient.resourceName` | string |  |
| `customerClient.status` | string |  |
| `customerClient.timeZone` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-client-hierarchy.md) for the provider-specific parameters and requirements.

