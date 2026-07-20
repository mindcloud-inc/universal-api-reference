# Create Customer with MRPeasy

Creates a new customer in MRPeasy.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Create Customer](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Customer name. |
| `code` | body | `string` | no | Optional customer code. |
| `contact_data` | body | `array<object>` | yes | Array of MRPeasy contact_data objects. |
