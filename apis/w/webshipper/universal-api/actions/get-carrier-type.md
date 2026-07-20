# Webshipper: Get Carrier Type

Retrieves a carrier type from Webshipper.

```
GET https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/get-carrier-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/get-carrier-type?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/get-carrier-type?${params}`, {
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
| `id` | string | no | The carrier type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "barcode_customer_notification_mail_template_id": "string",
      "barcode_mail": "string",
      "beta": true,
      "carrier_code": "string",
      "carrier_group_id": "string",
      "colli_type_support": "string",
      "fulfillment_logo": "string",
      "hide": true,
      "id": "string",
      "is_edi": true,
      "list_logo": "string",
      "name": "Ava Chen",
      "onboarding_url": "https://example.com",
      "rate_quote_validation": true,
      "require_ftp_configuration_id": true,
      "required_details": "string",
      "requires_approval": true,
      "requires_dutiable": "string",
      "shipment_updates_limit_minutes": 1,
      "show_send_time": "string",
      "supports_deletion": true,
      "supports_documents": true,
      "supports_pickup": true,
      "supports_price_pdf_upload": true,
      "supports_price_quoting": "string",
      "supports_shadow_bookings": true,
      "supports_shipment_updates": true,
      "supports_test_mode": true,
      "supports_tracking": true,
      "supports_zpl": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `barcode_customer_notification_mail_template_id` | string |  |
| `barcode_mail` | string |  |
| `beta` | boolean |  |
| `carrier_code` | string |  |
| `carrier_group_id` | string |  |
| `colli_type_support` | string |  |
| `fulfillment_logo` | string |  |
| `hide` | boolean |  |
| `id` | string |  |
| `is_edi` | boolean |  |
| `list_logo` | string |  |
| `name` | string |  |
| `onboarding_url` | string |  |
| `rate_quote_validation` | boolean |  |
| `require_ftp_configuration_id` | boolean |  |
| `required_details` | string |  |
| `requires_approval` | boolean |  |
| `requires_dutiable` | string |  |
| `shipment_updates_limit_minutes` | number |  |
| `show_send_time` | string |  |
| `supports_deletion` | boolean |  |
| `supports_documents` | boolean |  |
| `supports_pickup` | boolean |  |
| `supports_price_pdf_upload` | boolean |  |
| `supports_price_quoting` | string |  |
| `supports_shadow_bookings` | boolean |  |
| `supports_shipment_updates` | boolean |  |
| `supports_test_mode` | boolean |  |
| `supports_tracking` | boolean |  |
| `supports_zpl` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `GET /carrier_types/:id` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-carrier-type.md) for the provider-specific parameters and requirements.

