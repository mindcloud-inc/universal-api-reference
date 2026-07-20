# Update Property Integration with EasyBroker

Updates a property integration status in EasyBroker.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/integration_partners/properties/:property_id/property_integration`
- **Base URL:** `https://api.easybroker.com/v1`
- **Official documentation:** [Update Property Integration](https://dev.easybroker.com/reference/patch_properties-property-id-property-integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `error_message` | body | `list<string>` | no | Required if status is failed. Error messages explaining why the listing could not be published or updated. |
| `listing_url` | body | `string` | no | Required if status is successful. The listing URL on your website. |
| `property_id` | path | `string` | yes | The EasyBroker property ID related to the listing on your website. |
| `status` | body | `string` | yes | The listing status on your website. |
