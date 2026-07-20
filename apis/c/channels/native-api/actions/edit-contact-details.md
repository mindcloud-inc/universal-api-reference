# Edit Contact Details with Channels

Updates existing contact details in Channels.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/contacts/{contactId}/details`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [Edit Contact Details](https://developers.channels.app/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | Contact ID whose details should be edited. |
| `details` | body | `object` | yes | Contact details object to replace or edit. |
