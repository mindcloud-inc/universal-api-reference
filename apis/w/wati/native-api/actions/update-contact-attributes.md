# Update Contact Attributes with Wati

Updates contact attributes for one contact in Wati.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/updateContactAttributes/:whatsappNumber`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [Update Contact Attributes](https://docs.wati.io/reference/post_api-v1-updatecontactattributes-whatsappnumber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whatsappNumber` | path | `string` | yes | Target contact phone number. |
| `customParams[]` | body | `array<object>` | yes | Custom attributes to update on the contact. |
