# Update Form Salesforce Action with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/form/integration/salesforce/actions/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Form Salesforce Action](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | ID of the Salesforce action to update. |
| `objectKey` | body | `string` | yes | Updated key of the Salesforce object. |
| `actionType` | body | `string` | yes | Updated type of Salesforce action. |
| `upsert` | body | `boolean` | yes | Updated flag for upsert action. |
| `createData[]` | body | `array` | yes | Updated array of Salesforce fields and corresponding form fields for create/update. |
| `matchData[]` | body | `array` | yes | Updated array of Salesforce fields and corresponding form fields for matching in upsert. |
