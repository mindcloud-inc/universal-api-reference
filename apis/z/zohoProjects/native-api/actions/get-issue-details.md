# Get Issue Details with Zoho Projects

Retrieves issue details from Zoho Projects.

## Endpoint

- **Method:** `GET`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/issues/[:ISSUEID]`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [Get Issue Details](https://projectsapi.zoho.com/api-docs#issues_get-issue-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Zoho Projects portal ID. |
| `PROJECTID` | path | `string` | yes | Zoho Projects project ID. |
| `ISSUEID` | path | `string` | yes | Zoho Projects issue ID. |
