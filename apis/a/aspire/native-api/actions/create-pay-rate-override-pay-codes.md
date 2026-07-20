# Create Pay Rate Override Pay Codes with Aspire

Creates a new pay rate override pay code in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `PayRateOverridePayCodes`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Pay Rate Override Pay Codes](https://guide.youraspire.com/apidocs/payrates-5)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PayRateID` | body | `list<number>` | no |
| `PayCodeID` | body | `list<number>` | no |
| `OverrideRate` | body | `number` | no |
