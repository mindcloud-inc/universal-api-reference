# Delete Contact Alternative MSISDN with Channels

Deletes an alternative contact phone number from Channels.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/contacts/{contactId}/alternative-msisdns/{msisdnId}`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [Delete Contact Alternative MSISDN](https://developers.channels.app/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | Contact ID that owns the alternative MSISDN. |
| `msisdnId` | path | `number` | yes | Alternative MSISDN ID to delete. |
