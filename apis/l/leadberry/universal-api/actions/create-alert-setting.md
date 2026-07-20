# Leadberry: Create Alert Setting



```
POST https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/create-alert-setting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadberry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/create-alert-setting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/create-alert-setting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aid` | string | no | Leadberry account ID for the selected alert view. |
| `emails[]` | string | no | Email addresses that should receive the alert. |
| `freq` | string | no | Leadberry alert frequency such as default, everyday, everyweek, or realtime. |
| `pid` | string | no | Leadberry profile ID for the selected alert view. |
| `url` | string | no | Alert URL value used by Leadberry. The bundle sets this to an empty string for the standard flow. |
| `wid` | string | no | Leadberry website ID for the selected alert view. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadberry API returns.

## Native endpoint

Through the native Leadberry API, this operation is `POST /data/saveNewAlertSetting` (base URL `https://app.leadberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-alert-setting.md) for the provider-specific parameters and requirements.

