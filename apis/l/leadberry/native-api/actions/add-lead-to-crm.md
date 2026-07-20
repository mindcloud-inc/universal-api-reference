# Add Lead To CRM with Leadberry

## Endpoint

- **Method:** `POST`
- **Path:** `/data/addToCRM`
- **Base URL:** `https://app.leadberry.com`
- **Official documentation:** [Add Lead To CRM](https://www.leadberry.com/integrations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Leadberry CRM connection ID to use for the sync. |
| `visibleUrlId` | body | `string` | no | Leadberry visible URL ID for the lead to send. |
