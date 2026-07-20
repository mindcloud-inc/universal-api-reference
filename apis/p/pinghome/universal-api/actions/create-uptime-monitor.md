# Pinghome: Create Uptime Monitor

Creates a new uptime monitor in Pinghome.

```
POST https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-uptime-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-uptime-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "gracePeriod": "0",
  "isAdvanced": "false",
  "method": "GET",
  "name": "Pinghome Homepage",
  "notFollowRedirect": "false",
  "recoveryPeriod": "0",
  "regions[]": "eu-central-1",
  "serviceId": "b4cc5758-7443-40f6-8009-55961a3cfc09",
  "skipSslError": "false",
  "type": "http",
  "url": "https://www.pinghome.io"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-uptime-monitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "gracePeriod": "0",
    "isAdvanced": "false",
    "method": "GET",
    "name": "Pinghome Homepage",
    "notFollowRedirect": "false",
    "recoveryPeriod": "0",
    "regions[]": "eu-central-1",
    "serviceId": "b4cc5758-7443-40f6-8009-55961a3cfc09",
    "skipSslError": "false",
    "type": "http",
    "url": "https://www.pinghome.io"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `gracePeriod` | number | yes | Grace period before an incident is triggered. Example: `0`. |
| `isAdvanced` | boolean | yes | Whether advanced monitoring mode is enabled. Example: `false`. |
| `method` | string | yes | The HTTP method used for the monitor request. Example: `GET`. |
| `name` | string | yes | The name of the uptime monitor. Example: `Pinghome Homepage`. |
| `notFollowRedirect` | boolean | yes | Whether redirects should not be followed. Example: `false`. |
| `recoveryPeriod` | number | yes | Recovery period before the monitor is considered healthy again. Example: `0`. |
| `regions[]` | array<string> | yes | The AWS regions that should run checks for this monitor. Example: `eu-central-1`. |
| `serviceId` | string | yes | The service id that owns the uptime monitor. Example: `b4cc5758-7443-40f6-8009-55961a3cfc09`. |
| `skipSslError` | boolean | yes | Whether SSL certificate errors should be ignored. Example: `false`. |
| `type` | string | yes | The monitor protocol type, such as http. Example: `http`. |
| `url` | string | yes | The URL to monitor. Example: `https://www.pinghome.io`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `POST /resource-cmd/v1/resource` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-uptime-monitor.md) for the provider-specific parameters and requirements.

