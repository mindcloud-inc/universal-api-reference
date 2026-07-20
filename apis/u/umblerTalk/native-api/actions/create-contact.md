# Create Contact with Umbler Talk

Creates a new contact in Umbler Talk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Create Contact](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Contact name. |
| `organizationId` | body | `string` | yes | The organization ID. |
| `phoneNumber` | body | `string` | yes | Contact phone number. |
