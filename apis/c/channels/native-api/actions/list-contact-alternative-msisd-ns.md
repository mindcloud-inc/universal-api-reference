# List Contact Alternative MSISDNs with Channels

Retrieves alternative contact phone numbers from Channels.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/contacts/{contactId}/alternative-msisdns`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [List Contact Alternative MSISDNs](https://developers.channels.app/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | Contact ID whose alternative MSISDNs should be returned. |
