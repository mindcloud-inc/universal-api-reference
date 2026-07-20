# Get Record Count with Zoho People

Retrieves record count for a Zoho People form.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/forms/:formLinkName/getRecordCount`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Get Record Count](https://www.zoho.com/people/api/get-record-count.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formLinkName` | path | `string` | yes | Zoho People formLinkName. Example: employee. |
