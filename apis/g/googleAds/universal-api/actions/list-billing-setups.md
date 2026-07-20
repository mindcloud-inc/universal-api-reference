# Google Ads: List Billing Setups

Retrieves billing setups from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-billing-setups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-billing-setups?connectionId=$CONNECTION_ID&customerId=1234567890&query=SELECT%20billing_setup.id%2C%20billing_setup.status%20FROM%20billing_setup%20LIMIT%2050" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "query": "SELECT billing_setup.id, billing_setup.status FROM billing_setup LIMIT 50"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-billing-setups?${params}`, {
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
| `customerId` | list | yes | Customer ID that owns the Google Ads resources (without dashes). Example: `1234567890`. |
| `query` | string | yes | GAQL query to list billing setup resources. Default: `SELECT billing_setup.id, billing_setup.status, billing_setup.start_date_time, billing_setup.end_date_time FROM billing_setup ORDER BY billing_setup.id DESC LIMIT 50`. Example: `SELECT billing_setup.id, billing_setup.status FROM billing_setup LIMIT 50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingSetup": {
        "id": "string",
        "resourceName": "Ava Chen",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingSetup.id` | string |  |
| `billingSetup.resourceName` | string |  |
| `billingSetup.status` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-billing-setups.md) for the provider-specific parameters and requirements.

