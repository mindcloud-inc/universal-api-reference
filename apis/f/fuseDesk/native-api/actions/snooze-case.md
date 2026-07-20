# Snooze Case with FuseDesk

Snoozes an existing FuseDesk case until a later time.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/cases/:caseId/snooze`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Snooze Case](https://documenter.getpostman.com/view/11014835/SztBc8ix#ba5d9b6a-2cb6-4d74-a798-a69baaa9ce27)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caseId` | path | `number` | yes | The FuseDesk case ID to snooze. |
| `until` | body | `date` | yes | ISO 8601 datetime until which the case remains snoozed. |
