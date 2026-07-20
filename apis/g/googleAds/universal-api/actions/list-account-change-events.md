# Google Ads: List Account Change Events

Retrieves account change events from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-account-change-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-account-change-events?connectionId=$CONNECTION_ID&customerId=1234567890&query=SELECT%20change_event.change_date_time%2C%20change_event.change_resource_name%20FROM%20change_event%20WHERE%20change_event.change_date_time%20DURING%20LAST_7_DAYS%20LIMIT%20100" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "query": "SELECT change_event.change_date_time, change_event.change_resource_name FROM change_event WHERE change_event.change_date_time DURING LAST_7_DAYS LIMIT 100"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-account-change-events?${params}`, {
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
| `query` | string | yes | GAQL query for change_event tracking. Default: `SELECT change_event.resource_name, change_event.change_date_time, change_event.change_resource_name, change_event.change_resource_type, change_event.user_email FROM change_event WHERE change_event.change_date_time DURING LAST_7_DAYS ORDER BY change_event.change_date_time DESC LIMIT 1000`. Example: `SELECT change_event.change_date_time, change_event.change_resource_name FROM change_event WHERE change_event.change_date_time DURING LAST_7_DAYS LIMIT 100`. |

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

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-change-events.md) for the provider-specific parameters and requirements.

