# Get Lead with Tiledesk

Retrieves a lead from the current Tiledesk project.

## Endpoint

- **Method:** `GET`
- **Path:** `/{projectId}/leads/:leadId`
- **Base URL:** `https://api.tiledesk.com/v3`
- **Official documentation:** [Get Lead](https://developer.tiledesk.com/apis/rest-api/leads#get-a-lead-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadId` | path | `string` | yes | The lead identifier. |
