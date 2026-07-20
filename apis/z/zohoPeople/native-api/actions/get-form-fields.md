# Get Form Fields with Zoho People

Retrieves fields for a Zoho People form.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/forms/:formLinkName/components`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Get Form Fields](https://www.zoho.com/people/api/forms-api/get-field-forms.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formLinkName` | path | `string` | yes | Zoho People formLinkName. Example: employee. |
