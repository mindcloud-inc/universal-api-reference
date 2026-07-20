# RotaCloud: List Settings

Lists account settings in RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attendance_pay_frequency": {},
      "attendance_record_breaks": {},
      "currency_symbol": {},
      "leave_requests_enabled": {},
      "leave_requests_notice_days": {},
      "mobile_clocking_enabled": {},
      "open_shift_claiming_enabled": {},
      "pay_codes": {},
      "rota_grouping": {},
      "shift_swaps_enabled": {},
      "time_format": {},
      "unavailability_requests_enabled": {},
      "webhook_signing_secret": {},
      "week_starts": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendance_pay_frequency` | object |  |
| `attendance_record_breaks` | object |  |
| `currency_symbol` | object |  |
| `leave_requests_enabled` | object |  |
| `leave_requests_notice_days` | object |  |
| `mobile_clocking_enabled` | object |  |
| `open_shift_claiming_enabled` | object |  |
| `pay_codes` | object |  |
| `rota_grouping` | object |  |
| `shift_swaps_enabled` | object |  |
| `time_format` | object |  |
| `unavailability_requests_enabled` | object |  |
| `webhook_signing_secret` | object |  |
| `week_starts` | object |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/settings` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-settings.md) for the provider-specific parameters and requirements.

