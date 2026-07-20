# Run Outstanding Invoice with Cheddar

Executes an outstanding invoice in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/run-outstanding/productCode/{productCode}/code/:customerCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Run Outstanding Invoice](https://docs.getcheddar.com/#run-an-outstanding-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Customer code from Cheddar. |
| `ccCardCode` | body | `string` | no | 3-4 digit card verification value. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
