# Update QR Code with Scanova

## Endpoint

- **Method:** `PUT`
- **Path:** `/qr/{qrid}/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Update QR Code](https://docs.scanova.io/api-reference/endpoint/qr_manager/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `qrid` | path | `string` | yes | QR Code ID |
| `name` | body | `string` | no | Name of the QR Code |
| `info` | body | `string` | no | JSON data to update QR code content. See [Components Reference](/api-reference/references/components) for detailed structure examples for each category. |
| `pattern_info` | body | `string` | no | JSON data to update QR code design. See [Pattern Info Reference](/api-reference/references/pattern-info) for complete customization options and field values. |
| `expire_on` | body | `date` | no | Expiration date and time for the QR code (advanced feature - requires plan quota) |
| `expire_on_text` | body | `string` | no | Custom HTML text to display when QR code is expired (advanced feature - requires plan quota) |
| `expire_on_timezone` | body | `string` | no | Timezone for expiration date (advanced feature - requires plan quota) |
| `high_accuracy_confirmation` | body | `boolean` | no | Enable high accuracy confirmation for location-based QR codes (advanced feature - requires plan quota) |
| `high_accuracy_geo_fencing` | body | `boolean` | no | Enable high accuracy geo-fencing for location-based QR codes (advanced feature - requires plan quota) |
| `high_accuracy_geo_fencing_config` | body | `object` | no | Configuration for high accuracy geo-fencing (advanced feature - requires plan quota) |
| `high_accuracy_mode` | body | `boolean` | no | Enable high accuracy mode for location-based QR codes (advanced feature - requires plan quota) |
| `high_accuracy_mode_text` | body | `string` | no | Text to display when requesting location access (advanced feature - requires plan quota) |
| `lead_list` | body | `number` | no | Lead list ID for capturing leads (advanced feature - requires plan quota). Set to null to remove lead list. |
| `minimum_age` | body | `number` | no | Minimum age requirement for accessing QR code content (advanced feature - requires plan quota) |
| `password` | body | `string` | no | Password protection for QR code access (advanced feature - requires plan quota) |
