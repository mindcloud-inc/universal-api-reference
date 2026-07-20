# Validate Bulk Sign Packages with SigningHub

Validates packages for bulk signing in SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages/SIGN/pre`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Validate Bulk Sign Packages](https://manuals.nsignhub.com/latest/Api/#tag/Document-Processing/operation/V4_Signing_ValidateBulkSignPackages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | The document package IDs to validate for bulk signing. |
