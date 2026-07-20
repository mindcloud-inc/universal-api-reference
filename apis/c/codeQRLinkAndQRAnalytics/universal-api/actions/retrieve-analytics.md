# CodeQR - Link and QR Analytics: Retrieve Analytics

Retrieves analytics from CodeQR.

```
GET https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/retrieve-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeQR - Link and QR Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/retrieve-analytics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/retrieve-analytics?${params}`, {
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
| `interval` | string | no | The interval to retrieve analytics for. Default: `24h`. |
| `event` | string | no | The event type to retrieve analytics for. Default: `clicks`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "leads": 1,
      "saleAmount": 1,
      "sales": 1,
      "scans": 1,
      "views": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number |  |
| `leads` | number |  |
| `saleAmount` | number |  |
| `sales` | number |  |
| `scans` | number |  |
| `views` | number |  |

## Native endpoint

Through the native CodeQR - Link and QR Analytics API, this operation is `GET /analytics` (base URL `https://api.codeqr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-analytics.md) for the provider-specific parameters and requirements.

