# Google Ads: List Account Change Status

Retrieves account change status from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-account-change-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-account-change-status?connectionId=$CONNECTION_ID&customerId=1234567890&query=SELECT%20change_status.resource_name%2C%20change_status.last_change_date_time%20FROM%20change_status%20WHERE%20change_status.last_change_date_time%20DURING%20LAST_7_DAYS%20LIMIT%20100" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "query": "SELECT change_status.resource_name, change_status.last_change_date_time FROM change_status WHERE change_status.last_change_date_time DURING LAST_7_DAYS LIMIT 100"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-account-change-status?${params}`, {
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
| `query` | string | yes | GAQL query for change_status tracking. Default: `SELECT change_status.resource_name, change_status.last_change_date_time, change_status.resource_type, change_status.resource_status FROM change_status WHERE change_status.last_change_date_time DURING LAST_7_DAYS ORDER BY change_status.last_change_date_time DESC LIMIT 1000`. Example: `SELECT change_status.resource_name, change_status.last_change_date_time FROM change_status WHERE change_status.last_change_date_time DURING LAST_7_DAYS LIMIT 100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changeStatus": {
        "lastChangeDateTime": "string",
        "resourceName": "Ava Chen",
        "resourceStatus": "string",
        "resourceType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changeStatus.lastChangeDateTime` | string |  |
| `changeStatus.resourceName` | string |  |
| `changeStatus.resourceStatus` | string |  |
| `changeStatus.resourceType` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-change-status.md) for the provider-specific parameters and requirements.

