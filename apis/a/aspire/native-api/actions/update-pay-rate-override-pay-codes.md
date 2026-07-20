# Update Pay Rate Override Pay Codes with Aspire

Updates an existing pay rate override pay code in your Aspire account.

## Endpoint

- **Method:** `PUT`
- **Path:** `PayRateOverridePayCodes`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Pay Rate Override Pay Codes](https://guide.youraspire.com/apidocs/payrates-5)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PayRateID` | body | `list<number>` | yes |
| `PayCodeID` | body | `list` | yes |
| `OverrideRate` | body | `number` | no |
