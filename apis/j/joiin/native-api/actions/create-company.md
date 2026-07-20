# Create Company with Joiin

Creates a company in Joiin.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/companies`
- **Base URL:** `https://app-api.joiin.co`
- **Official documentation:** [Create Company](https://app.joiin.co/reference/create_company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The company name. |
| `externalId` | body | `string` | no | An external identifier for the company. |
| `sourceSystem` | body | `string` | yes | The source system for the imported company data. |
| `currency` | body | `string` | yes | The company currency code, for example USD. |
| `fiscalYearStartMonth` | body | `string` | yes | The month in which the company's fiscal year starts. |
| `ownershipShare` | body | `number` | no | The ownership share for the company. |
| `accounts[]` | body | `array<object>` | yes | The accounts array to import into Joiin. |
| `valueFormat` | body | `string` | yes | The format of the imported account values. |
