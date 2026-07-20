# Add Tags to Contact with Dripcel

Updates a contact to add tags in Dripcel.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:cell/tag/add`
- **Base URL:** `https://api.dripcel.com`
- **Official documentation:** [Add Tags to Contact](https://docs.dripcel.com/API/contacts#add-or-remove-tags-from-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cell` | path | `string` | yes | — |
| `tag_ids[]` | body | `array<string>` | no | The tag IDs to add to the contact. |
| `tags[]` | body | `array<string>` | no | The tag names to add to the contact. |
| `create_missing_contact` | body | `boolean` | no | Create the contact if it does not exist before adding tags. |
