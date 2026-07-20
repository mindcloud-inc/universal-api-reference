# Create Pay Codes with Aspire

Creates a new pay code in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `PayCodes`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Pay Codes](https://guide.youraspire.com/apidocs/paycodes-10)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ExcludeFromOT` | body | `boolean` | no | Format: `toggle`. |
| `OTPaycode` | body | `boolean` | no | Format: `toggle`. |
| `Active` | body | `boolean` | no | Format: `toggle`. |
| `FixedRate` | body | `number` | no | — |
| `PayCode` | body | `string` | no | — |
| `PayCodeName` | body | `string` | no | — |
| `PayCodeType` | body | `string` | no | — |
| `PremiumDollars` | body | `number` | no | — |
| `PremiumPercent` | body | `number` | no | — |
