# Satori Cyber: Get Authorization Analytics Metrics

Retrieves authorization analytics metrics from Satori Cyber.

```
GET https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/get-authorization-analytics-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Satori Cyber `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/get-authorization-analytics-metrics?connectionId=$CONNECTION_ID&accountId=acc_12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "acc_12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/get-authorization-analytics-metrics?${params}`, {
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
| `accountId` | string | yes | Satori account ID. Example: `acc_12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asset_count": 1,
      "cloud_account_count": 1,
      "governed_authorization_percent": 1,
      "identity_count": 1,
      "monitored_data_stores_count": 1,
      "total_data_stores_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asset_count` | number |  |
| `cloud_account_count` | number |  |
| `governed_authorization_percent` | number |  |
| `identity_count` | number |  |
| `monitored_data_stores_count` | number |  |
| `total_data_stores_count` | number |  |

## Native endpoint

Through the native Satori Cyber API, this operation is `GET /api/v1/authorization-analytics/:accountId/metrics` (base URL `https://app.satoricyber.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authorization-analytics-metrics.md) for the provider-specific parameters and requirements.

