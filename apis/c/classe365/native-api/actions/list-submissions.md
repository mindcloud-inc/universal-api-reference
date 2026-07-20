# List Submissions with Classe365

Retrieves a list of submissions from Classe365.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/getSubmissionsData`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [List Submissions](https://speca.io/classe365/academics#get-submissions-deta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | JSON string filter for submissions. |
| `page` | query | `string` | no | JSON string with recordsPerPage and pageNo. |
