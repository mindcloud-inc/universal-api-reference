# Google Ads: List Customer Label Assignments

Retrieves customer label assignments from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-label-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-label-assignments?connectionId=$CONNECTION_ID&customerId=1234567890&query=SELECT%20customer_label.customer%2C%20customer_label.label%20FROM%20customer_label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "query": "SELECT customer_label.customer, customer_label.label FROM customer_label"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-customer-label-assignments?${params}`, {
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
| `query` | string | yes | GAQL query for customer_label assignments. Default: `SELECT customer_label.resource_name, customer_label.customer, customer_label.label FROM customer_label`. Example: `SELECT customer_label.customer, customer_label.label FROM customer_label`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldMask": "string",
      "queryResourceConsumption": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldMask` | string |  |
| `queryResourceConsumption` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-label-assignments.md) for the provider-specific parameters and requirements.

