# Add Contact Alternative MSISDN with Channels

Creates an alternative contact phone number in Channels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts/{contactId}/alternative-msisdns`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [Add Contact Alternative MSISDN](https://developers.channels.app/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | Contact ID to add an alternative MSISDN to. |
| `msisdn` | body | `string` | yes | Phone number to add as an alternative MSISDN. |
