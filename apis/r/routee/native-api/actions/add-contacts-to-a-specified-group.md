# Add Contacts to a specified group with Routee

Adds contacts to a specified group in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/my/:name/contacts`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Add Contacts to a specified group](https://docs.routee.net/reference/add-contacts-to-a-specified-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The name of the group |
| `contacts[]` | body | `array<string>` | yes | The contacts' ids. |
