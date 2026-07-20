# Create Pay Rate with Aspire

Creates a new pay code in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `PayRates`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Pay Rate](https://guide.youraspire.com/apidocs/payrates-6)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `effectiveDate` | body | `string` | yes |
| `hourlyBasePay` | body | `string` | yes |
| `contactId` | body | `list<string>` | yes |
| `burdenPercent` | body | `string` | yes |
