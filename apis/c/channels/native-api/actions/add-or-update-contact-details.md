# Add Or Update Contact Details with Channels

Updates contact details in Channels, or creates them if missing.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts/{contactId}/details`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [Add Or Update Contact Details](https://developers.channels.app/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | Contact ID whose details should be added or updated. |
| `details` | body | `object` | yes | Contact details object to add or update. |
