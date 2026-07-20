# UpGuard: Stop Monitoring Vendor

Stops monitoring a vendor in UpGuard.

```
DELETE https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/stop-monitoring-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/stop-monitoring-vendor?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/stop-monitoring-vendor?${params}`, {
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
| `hostname` | string | no | The hostname of the vendor to stop monitoring when no vendor ID is provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native UpGuard API, this operation is `POST /vendor/unmonitor` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-monitoring-vendor.md) for the provider-specific parameters and requirements.

