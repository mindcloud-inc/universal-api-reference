# Download Verification Results with Verify550

Downloads verification result files from Verify550.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobexport/:jobId`
- **Base URL:** `https://app.verify550.com/api`
- **Official documentation:** [Download Verification Results](https://verify550.com/documentation/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Verify550 bulk verification job ID. |
| `categories[]` | query | `array<string>` | no | Optional result categories to include in the export. Send multiple values as a string separated by `,`. |
| `format` | query | `string` | no | Export file format. Accepted values: `csv`, `xlsx`. |
