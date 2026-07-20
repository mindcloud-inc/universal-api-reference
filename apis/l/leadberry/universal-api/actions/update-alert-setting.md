# Leadberry: Update Alert Setting



```
PUT https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/update-alert-setting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadberry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/update-alert-setting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/update-alert-setting', {
  method: 'PUT',
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
| `aid` | string | no | Leadberry account ID for the alert view. |
| `alert_setting_id` | string | no | Leadberry alert setting identifier. |
| `alert_url_id` | string | no | Leadberry alert URL identifier. |
| `emails[]` | string | no | Email addresses for the alert. |
| `freq` | string | no | Leadberry alert frequency value. |
| `pid` | string | no | Leadberry profile ID for the alert view. |
| `type` | string | no | Leadberry alert email type, such as default or custom. |
| `url` | string | no | Alert URL value. |
| `wid` | string | no | Leadberry website ID for the alert view. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadberry API returns.

## Native endpoint

Through the native Leadberry API, this operation is `POST /data/updateAlertSetting` (base URL `https://app.leadberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-alert-setting.md) for the provider-specific parameters and requirements.

