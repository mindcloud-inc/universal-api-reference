# SmartReach: Get Email Setting

Retrieves an email setting from SmartReach.

```
GET https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/get-email-setting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/get-email-setting?connectionId=$CONNECTION_ID&emailSettingId=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailSettingId": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/get-email-setting?${params}`, {
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
| `emailSettingId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email_setting": {
        "email": "ava@example.com",
        "id": "ava@example.com",
        "service_provider": "ava@example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email_setting.email` | string |  |
| `email_setting.id` | string |  |
| `email_setting.service_provider` | string |  |

## Native endpoint

Through the native SmartReach API, this operation is `GET /email_settings/:email_setting_id` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-setting.md) for the provider-specific parameters and requirements.

