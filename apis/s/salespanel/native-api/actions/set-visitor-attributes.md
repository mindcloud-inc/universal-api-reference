# Set Visitor Attributes with Salespanel

Updates custom visitor attributes in Salespanel.

## Endpoint

- **Method:** `POST`
- **Path:** `/visitor-attributes/`
- **Base URL:** `https://salespanel.io/api/v1`
- **Official documentation:** [Set Visitor Attributes](https://salespanel.io/docs/#set-visitor-attributes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `visitor_identifier` | body | `string` | yes | Contact ID or email of the visitor. |
| `visitor_attributes` | body | `object` | yes | Key-value pairs to set for the visitor. |
| `create_new` | body | `boolean` | no | Create a new visitor if the email does not already exist. |
