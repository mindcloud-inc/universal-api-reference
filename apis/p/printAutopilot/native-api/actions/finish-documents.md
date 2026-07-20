# Finish Documents with Print Autopilot

Updates document statuses in Print Autopilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/finish-print-jobs`
- **Base URL:** `https://printautopilot.com/api`
- **Official documentation:** [Finish Documents](https://documenter.getpostman.com/view/1334461/TW6wJonb#a8422cc6-d08f-4b47-9e1e-418a6be82a6e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items[]` | body | `array<object>` | no | Document status objects to finish. |
| `items[].id` | body | `number` | no | — |
| `items[].state` | body | `string` | no | — |
| `err_msg` | body | `string` | no | Error message when the document state is failed. |
