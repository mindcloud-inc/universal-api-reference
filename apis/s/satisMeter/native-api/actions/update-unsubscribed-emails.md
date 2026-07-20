# Update Unsubscribed Emails with SatisMeter

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/project-unsubscribes/:projectId`
- **Base URL:** `https://app.satismeter.com`
- **Official documentation:** [Update Unsubscribed Emails](https://support.satismeter.com/hc/en-us/articles/6980458958995-Unsubscribe-email-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.emails` | body | `list<string>` | yes | Complete unsubscribe list to persist for the project. Provide the full desired set of unsubscribed email addresses. |
| `projectId` | path | `string` | yes | Project ID. |
