# List Automation Queues with Easymailing

Retrieves automation queues from Easymailing.

## Endpoint

- **Method:** `GET`
- **Path:** `/automations/{{automationUuid}}/automation_queues`
- **Base URL:** `https://api.easymailing.com`
- **Official documentation:** [List Automation Queues](https://developers.easymailing.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `automationUuid` | path | `string` | yes | Automation UUID. |
