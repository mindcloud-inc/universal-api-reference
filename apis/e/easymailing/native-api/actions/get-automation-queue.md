# Get Automation Queue with Easymailing

Retrieves an automation queue from Easymailing.

## Endpoint

- **Method:** `GET`
- **Path:** `/automations/{{automationUuid}}/automation_queues/{{uuid}}`
- **Base URL:** `https://api.easymailing.com`
- **Official documentation:** [Get Automation Queue](https://developers.easymailing.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `automationUuid` | path | `string` | yes | Automation UUID. |
| `uuid` | path | `string` | yes | Automation queue UUID. |
