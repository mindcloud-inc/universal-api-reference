# List Form Views with Zoho People

Retrieves views for a Zoho People form.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/forms/:formLinkName/views`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [List Form Views](https://www.zoho.com/people/api/fetch-view.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formLinkName` | path | `string` | yes | Zoho People formLinkName. Example: employee. |
