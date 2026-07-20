# Revise Record with Vtiger CRM

Updates an existing record in Vtiger CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/revise`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Revise Record](https://vtap.vtiger.com/platform/rest-apis.html#revise)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `element` | query | `string` | yes | JSON object string including the id and fields to update. |
