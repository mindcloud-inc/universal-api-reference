# Update Contact with Polaria

Updates an existing contact in Polaria.

## Endpoint

- **Method:** `PUT`
- **Path:** `/widgets/[:api_key]/contacts/[:id]`
- **Base URL:** `https://app.polaria.ai/rest/v2`
- **Official documentation:** [Update Contact](https://help.polaria.ai/hc/rest-api-contacts/put-widgets-api_key-contacts-id-update-a-contact?lang=en)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_key` | path | `string` | yes | The Polaria widget API key for the target brand. |
| `id` | path | `string` | yes | The ID of the contact to update. |
| `email` | body | `string` | no | — |
