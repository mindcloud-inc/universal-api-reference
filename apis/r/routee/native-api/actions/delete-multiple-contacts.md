# Delete multiple contacts with Routee

Deletes multiple contacts from your Routee account.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts/my`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Delete multiple contacts](https://docs.routee.net/reference/delete-multiple-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<string>` | yes | The ids of the contacts that will be deleted. |
