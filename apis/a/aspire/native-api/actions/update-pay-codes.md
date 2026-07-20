# Update Pay Codes with Aspire

Updates an existing pay code in your Aspire account.

## Endpoint

- **Method:** `PUT`
- **Path:** `PayCodes`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Pay Codes](https://guide.youraspire.com/apidocs/paycodes-11)

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
