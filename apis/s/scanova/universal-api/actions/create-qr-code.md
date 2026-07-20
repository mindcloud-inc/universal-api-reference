# Scanova: Create QR Code



```
POST https://connect.mindcloud.co/v1/universal/scanova/latest/actions/create-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/create-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category": 1,
  "info": "string",
  "name": "Ava Chen",
  "qrType": "dy"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scanova/latest/actions/create-qr-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category": 1,
    "info": "string",
    "name": "Ava Chen",
    "qrType": "dy"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | number | yes | QR Code Category ID. See [Category List](/api-reference/references/category-list) for full reference. In Try it: 1=Website URL, 9=Custom Page, 10=App Store, 11=Google Map, 13=Document, 14=Wedding, 15=Social Media, 16=Audio, 17=Coupon, 18=Product, 19=Image, 20=Event, 23=App Deep Link, 24=Business Card, 25=Restaurant, 26=Feedback, 27=Real Estate, 28=Link Page, 31=GS1, 44=Restaurant. |
| `info` | string | yes | JSON data to create QR code. See [Components Reference](/api-reference/references/components) for detailed structure examples for each category. |
| `name` | string | yes | Name of the QR Code |
| `qrType` | list | yes | QR code type. In Try it: dy=Dynamic (editable after creation), st=Static (fixed content). One of: `dy`, `st`. |
| `patternInfo` | string | no | JSON data to create design QR Code (optional). See [Pattern Info Reference](/api-reference/references/pattern-info) for complete customization options and field values. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customDomain` | number | no | Custom domain ID for the QR code (advanced feature - requires plan quota) |
| `expireOn` | date | no | Expiration date and time for the QR code (advanced feature - requires plan quota) |
| `expireOnText` | string | no | Custom HTML text to display when QR code is expired (advanced feature - requires plan quota) |
| `expireOnTimezone` | string | no | Timezone for expiration date (advanced feature - requires plan quota) |
| `highAccuracyConfirmation` | boolean | no | Enable high accuracy confirmation for location-based QR codes (advanced feature - requires plan quota) |
| `highAccuracyGeoFencing` | boolean | no | Enable high accuracy geo-fencing for location-based QR codes (advanced feature - requires plan quota) |
| `highAccuracyGeoFencingConfig` | object | no | Configuration for high accuracy geo-fencing (advanced feature - requires plan quota) |
| `highAccuracyMode` | boolean | no | Enable high accuracy mode for location-based QR codes (advanced feature - requires plan quota) |
| `highAccuracyModeText` | string | no | Text to display when requesting location access (advanced feature - requires plan quota) |
| `leadList` | number | no | Lead list ID for capturing leads (advanced feature - requires plan quota) |
| `minimumAge` | number | no | Minimum age requirement for accessing QR code content (advanced feature - requires plan quota) |
| `password` | string | no | Password protection for QR code access (advanced feature - requires plan quota) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ai_qr_code": "string",
      "category": {},
      "created": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "custom_form_response_count": 1,
      "dynamic_url_object": {},
      "id": 1,
      "info": "string",
      "is_active": true,
      "is_age_restricted": true,
      "is_designer": true,
      "is_password_protected": true,
      "is_qr_scannable": true,
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "password": "string",
      "pattern_info": "string",
      "pattern_type": "string",
      "qr_type": "string",
      "qr_type_display": "string",
      "qrid": "string",
      "restaurant_feedback_response_count": 1,
      "rsvp_form_response_count": 1,
      "svg_code": "string",
      "tags_list": [
        "string"
      ],
      "thumbnail": "string",
      "version": 1,
      "wallet_pass_info": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_qr_code` | string |  |
| `category` | object |  |
| `created` | date |  |
| `created_by` | string |  |
| `custom_form_response_count` | number |  |
| `dynamic_url_object` | object |  |
| `id` | number |  |
| `info` | string |  |
| `is_active` | boolean |  |
| `is_age_restricted` | boolean |  |
| `is_designer` | boolean |  |
| `is_password_protected` | boolean |  |
| `is_qr_scannable` | boolean |  |
| `modified` | date |  |
| `name` | string |  |
| `password` | string |  |
| `pattern_info` | string |  |
| `pattern_type` | string |  |
| `qr_type` | string |  |
| `qr_type_display` | string |  |
| `qrid` | string |  |
| `restaurant_feedback_response_count` | number |  |
| `rsvp_form_response_count` | number |  |
| `svg_code` | string |  |
| `tags_list` | array<string> |  |
| `thumbnail` | string |  |
| `version` | number |  |
| `wallet_pass_info` | string |  |

## Native endpoint

Through the native Scanova API, this operation is `POST /qr/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-qr-code.md) for the provider-specific parameters and requirements.

