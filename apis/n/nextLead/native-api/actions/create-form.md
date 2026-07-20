# Create Form with NextLead

Creates a new audience list form in NextLead.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/receive/forms/create-form`
- **Base URL:** `https://dashboard.nextlead.app`
- **Official documentation:** [Create Form](https://dashboard.nextlead.app/en/api-documentation#receive-form-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Form name. |
| `fields[]` | body | `array<object>` | yes | Array of form field definitions. |
