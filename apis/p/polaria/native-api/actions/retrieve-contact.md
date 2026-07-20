# Retrieve Contact with Polaria

Retrieves a contact from Polaria.

## Endpoint

- **Method:** `GET`
- **Path:** `/widgets/[:api_key]/contacts/[:id]`
- **Base URL:** `https://app.polaria.ai/rest/v2`
- **Official documentation:** [Retrieve Contact](https://help.polaria.ai/hc/rest-api-contacts/get-widgets-api_key-contacts-id-retrieve-a-contact?lang=en)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_key` | path | `string` | yes | The Polaria widget API key for the target brand. |
| `id` | path | `string` | yes | The ID of the contact to retrieve. |
