# Verify Contact with Sendblue

Sends a verification message to a contact in Sendblue.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/contacts/verify`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Verify Contact](https://docs.sendblue.com/api/resources/contacts/methods/verify/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | yes | Phone number to verify. |
