# Get Form Fields with FillFaster

Retrieves form fields from FillFaster by form ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/getFormFields`
- **Base URL:** `https://api.fillfaster.com`
- **Official documentation:** [Get Form Fields](https://documenter.getpostman.com/view/18912453/2s8ZDVZ3UJ#896e6612-7996-4865-8a84-12f012e74774)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formUID` | body | `string` | yes | FillFaster form identifier to inspect. |
