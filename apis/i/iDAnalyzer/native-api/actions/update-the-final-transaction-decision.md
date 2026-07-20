# Update the final transaction decision with ID Analyzer

Updates a saved transaction decision in ID Analyzer.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/transaction/:transactionId`
- **Base URL:** `https://api2.idanalyzer.com`
- **Official documentation:** [Update the final transaction decision](https://developer.idanalyzer.com/reference/patch-transaction-transactionid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `decision` | body | `string` | yes | Manual review decision. |
| `transactionId` | path | `string` | yes | Saved transaction ID. |
