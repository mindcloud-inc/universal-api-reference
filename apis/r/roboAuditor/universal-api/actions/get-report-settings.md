# RoboAuditor: Get Report Settings



```
GET https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/get-report-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RoboAuditor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/get-report-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/get-report-settings?${params}`, {
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
| `domainId` | string | no | Domain identifier for report settings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "report_manager_settings": {},
      "user_recommendations": {},
      "user_short_recommendations": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `report_manager_settings` | object |  |
| `user_recommendations` | object |  |
| `user_short_recommendations` | object |  |

## Native endpoint

Through the native RoboAuditor API, this operation is `GET /settings/report` (base URL `https://app.siteauditor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report-settings.md) for the provider-specific parameters and requirements.

