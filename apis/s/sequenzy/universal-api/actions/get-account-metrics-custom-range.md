# Sequenzy: Get Account Metrics (Custom Range)

Retrieves account engagement metrics from Sequenzy for a custom range.

```
GET https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-account-metrics-custom-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sequenzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-account-metrics-custom-range?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-account-metrics-custom-range?${params}`, {
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
| `end` | string | no | End of the custom time range in ISO 8601 format. |
| `start` | string | no | Start of the custom time range in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "stats": {
        "clicked": 1,
        "clickRate": 1,
        "delivered": 1,
        "deliveryRate": 1,
        "opened": 1,
        "openRate": 1,
        "sent": 1,
        "unsubscribed": 1,
        "unsubscribeRate": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stats.clicked` | number |  |
| `stats.clickRate` | number |  |
| `stats.delivered` | number |  |
| `stats.deliveryRate` | number |  |
| `stats.opened` | number |  |
| `stats.openRate` | number |  |
| `stats.sent` | number |  |
| `stats.unsubscribed` | number |  |
| `stats.unsubscribeRate` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sequenzy API, this operation is `GET /metrics` (base URL `https://api.sequenzy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-metrics-custom-range.md) for the provider-specific parameters and requirements.

