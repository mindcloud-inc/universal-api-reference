# Log Custom Activity with Salespanel

Creates a custom activity in Salespanel for a visitor.

## Endpoint

- **Method:** `POST`
- **Path:** `/custom-activity/create/`
- **Base URL:** `https://salespanel.io/api/v1`
- **Official documentation:** [Log Custom Activity](https://salespanel.io/docs/#log-a-custom-activity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `visitor_identifier` | body | `string` | yes | Contact ID or email of the contact. |
| `category` | body | `string` | yes | Category for the custom activity. |
| `label` | body | `string` | yes | Label for the custom activity. |
| `activity_identifier` | body | `string` | no | Identifier for the custom activity. |
| `metadata` | body | `object` | no | Additional data provided for the custom activity. |
| `create_new` | body | `boolean` | no | Create a new visitor if the email does not already exist. |
