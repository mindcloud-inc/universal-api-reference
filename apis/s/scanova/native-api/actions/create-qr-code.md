# Create QR Code with Scanova

## Endpoint

- **Method:** `POST`
- **Path:** `/qr/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Create QR Code](https://docs.scanova.io/api-reference/endpoint/qr_manager/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `number` | yes | QR Code Category ID. See [Category List](/api-reference/references/category-list) for full reference. In Try it: 1=Website URL, 9=Custom Page, 10=App Store, 11=Google Map, 13=Document, 14=Wedding, 15=Social Media, 16=Audio, 17=Coupon, 18=Product, 19=Image, 20=Event, 23=App Deep Link, 24=Business Card, 25=Restaurant, 26=Feedback, 27=Real Estate, 28=Link Page, 31=GS1, 44=Restaurant. |
| `info` | body | `string` | yes | JSON data to create QR code. See [Components Reference](/api-reference/references/components) for detailed structure examples for each category. |
| `name` | body | `string` | yes | Name of the QR Code |
| `qr_type` | body | `list` | yes | QR code type. In Try it: dy=Dynamic (editable after creation), st=Static (fixed content). Accepted values: `dy`, `st`. |
| `pattern_info` | body | `string` | no | JSON data to create design QR Code (optional). See [Pattern Info Reference](/api-reference/references/pattern-info) for complete customization options and field values. |
| `custom_domain` | body | `number` | no | Custom domain ID for the QR code (advanced feature - requires plan quota) |
| `expire_on` | body | `date` | no | Expiration date and time for the QR code (advanced feature - requires plan quota) |
| `expire_on_text` | body | `string` | no | Custom HTML text to display when QR code is expired (advanced feature - requires plan quota) |
| `expire_on_timezone` | body | `string` | no | Timezone for expiration date (advanced feature - requires plan quota) |
| `high_accuracy_confirmation` | body | `boolean` | no | Enable high accuracy confirmation for location-based QR codes (advanced feature - requires plan quota) |
| `high_accuracy_geo_fencing` | body | `boolean` | no | Enable high accuracy geo-fencing for location-based QR codes (advanced feature - requires plan quota) |
| `high_accuracy_geo_fencing_config` | body | `object` | no | Configuration for high accuracy geo-fencing (advanced feature - requires plan quota) |
| `high_accuracy_mode` | body | `boolean` | no | Enable high accuracy mode for location-based QR codes (advanced feature - requires plan quota) |
| `high_accuracy_mode_text` | body | `string` | no | Text to display when requesting location access (advanced feature - requires plan quota) |
| `lead_list` | body | `number` | no | Lead list ID for capturing leads (advanced feature - requires plan quota) |
| `minimum_age` | body | `number` | no | Minimum age requirement for accessing QR code content (advanced feature - requires plan quota) |
| `password` | body | `string` | no | Password protection for QR code access (advanced feature - requires plan quota) |
