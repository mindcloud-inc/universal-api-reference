# Delete Webhook with Slottable

Deletes an existing webhook from Slottable.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/companies/:companyId/webhooks/:hookId`
- **Base URL:** `https://slottable.app/api/v1`
- **Official documentation:** [Delete Webhook](https://slottable.app/docs/p/integrations-and-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Company id returned by Slottable token details. |
| `hookId` | path | `number` | yes | Webhook id returned when creating a webhook. |
