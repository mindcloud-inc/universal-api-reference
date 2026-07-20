# Update Pay Rate with Aspire

## Endpoint

- **Method:** `PUT`
- **Path:** `PayRates`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Pay Rate](https://guide.youraspire.com/apidocs/payrates-7)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PayRateID` | body | `list<number>` | yes |
| `ContactID` | body | `list<number>` | yes |
| `effectiveDate` | body | `string` | yes |
| `hourlyBasePay` | body | `string` | no |
| `burdenPercent` | body | `string` | no |
