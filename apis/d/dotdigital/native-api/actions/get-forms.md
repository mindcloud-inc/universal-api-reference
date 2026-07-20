# Get Forms with Dotdigital

Retrieves all account forms from Dotdigital.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/surveys`
- **Base URL:** `https://r2-api.dotmailer.com`
- **Official documentation:** [Get Forms](https://developer.dotdigital.com/reference/get-forms)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignedToAddressBookOnly` | query | `boolean` | no | True returns only forms assigned from an address book. False returns only forms not assigned to an address book. |
