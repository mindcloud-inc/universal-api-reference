# Webshipper: List Carriers

Retrieves carriers from Webshipper.

```
GET https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-carriers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-carriers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-carriers?${params}`, {
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
      "alias": "string",
      "approved_service_codes": [
        "string"
      ],
      "attrs": [
        {}
      ],
      "barcode_notification_behavior": "string",
      "barcode_notification_mail": "string",
      "created_at": "string",
      "delete_at_carrier": true,
      "ftp_configuration_id": 1,
      "has_active_cost_sheet": true,
      "id": "string",
      "is_approved": true,
      "prefer_zpl": "string",
      "print_error_label": true,
      "service_parameter_enums": [
        "string"
      ],
      "services": [
        {}
      ],
      "test_mode": true,
      "type": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `approved_service_codes` | array<string> |  |
| `attrs` | array<object> |  |
| `barcode_notification_behavior` | string |  |
| `barcode_notification_mail` | string |  |
| `created_at` | string |  |
| `delete_at_carrier` | boolean |  |
| `ftp_configuration_id` | number |  |
| `has_active_cost_sheet` | boolean |  |
| `id` | string |  |
| `is_approved` | boolean |  |
| `prefer_zpl` | string |  |
| `print_error_label` | boolean |  |
| `service_parameter_enums` | array<string> |  |
| `services` | array<object> |  |
| `test_mode` | boolean |  |
| `type` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `GET /carriers` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-carriers.md) for the provider-specific parameters and requirements.

