# Delete Issue with Zoho Projects

Deletes an existing issue from Zoho Projects.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/issues/[:ISSUEID]`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [Delete Issue](https://projectsapi.zoho.com/api-docs#issues_delete-an-issue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Zoho Projects portal ID. |
| `PROJECTID` | path | `string` | yes | Zoho Projects project ID. |
| `ISSUEID` | path | `string` | yes | Zoho Projects issue ID. |
