# Remove Tags from Contact with Dripcel

Updates a contact to remove tags in Dripcel.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:cell/tag/remove`
- **Base URL:** `https://api.dripcel.com`
- **Official documentation:** [Remove Tags from Contact](https://docs.dripcel.com/API/contacts#add-or-remove-tags-from-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cell` | path | `string` | yes | — |
| `tag_ids[]` | body | `array<string>` | no | The tag IDs to remove from the contact. |
| `tags[]` | body | `array<string>` | no | The tag names to remove from the contact. |
