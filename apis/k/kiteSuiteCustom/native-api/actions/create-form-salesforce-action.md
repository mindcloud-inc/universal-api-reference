# Create Form Salesforce Action with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/form/integration/salesforce/actions`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Create Form Salesforce Action](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `form` | body | `string` | yes | ID of the form. |
| `objectKey` | body | `string` | yes | Key of the Salesforce object. |
| `actionType` | body | `string` | yes | Type of Salesforce action. |
| `upsert` | body | `boolean` | yes | Flag for upsert action. |
| `createData[]` | body | `array` | yes | Array of Salesforce fields and corresponding form fields for create/update. |
| `matchData[]` | body | `array` | yes | Array of Salesforce fields and corresponding form fields for matching in upsert. |
