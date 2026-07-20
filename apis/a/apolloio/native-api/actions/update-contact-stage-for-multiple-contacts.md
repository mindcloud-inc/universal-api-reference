# Update Contact Stage for Multiple Contacts with Apollo

Updates contact stages for multiple contacts in Apollo.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/contacts/update_stages`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Update Contact Stage for Multiple Contacts](https://docs.apollo.io/reference/update-contact-stage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_ids[]` | body | `array<string>` | yes | The Apollo IDs for the contacts that you want to update. To find contact IDs, call the Search for Contacts endpoint and identify the `id` value for the contact. Example: `66e34b81740c50074e3d1bd4` Send multiple values as a array. |
| `contact_stage_id` | body | `string<string>` | yes | The Apollo ID for the contact stage to which you want to assign the contacts. Call the List Contact Stages endpoint to retrieve a list of all the contact stage IDs available in your Apollo account. Example: `6095a710bd01d100a506d4af` |
