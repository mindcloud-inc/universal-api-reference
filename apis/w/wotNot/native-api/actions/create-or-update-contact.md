# Create Or Update Contact with WotNot

Creates or updates a contact in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/conversations`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Create Or Update Contact](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[0].custom_variables.company` | body | `string` | no | Optional company custom variable |
| `contacts[0].email` | body | `string` | no | Contact email. Either email or phone is required. |
| `contacts[0].name` | body | `string` | no | Contact name |
| `contacts[0].phone` | body | `string` | no | Contact phone. Either email or phone is required. |
