# Get Contact By Phone with Umbler Talk

Finds a contact in Umbler Talk by phone number.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts/phone/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Get Contact By Phone](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | query | `string` | yes | The organization ID. |
| `phoneNumber` | query | `string` | yes | The contact phone number. |
