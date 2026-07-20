# List Exportable Fields with MoreApp

Retrieves exportable submission fields from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/customers/{{customerId}}/forms/{{formId}}/submissions/export/fields`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [List Exportable Fields](https://docs.moreapp.com/docs/developer-docs/5eb67d5bdcd81-list-all-exportable-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `formId` | path | `string` | yes | MoreApp form identifier. |
