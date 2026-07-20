# Bulk Sign Packages with SigningHub

Signs packages in bulk in SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages/SIGN`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Bulk Sign Packages](https://manuals.nsignhub.com/latest/Api/#tag/Document-Processing/operation/V4_Signing_BulkSignDocuments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | The document package IDs to bulk sign. |
| `hand_signature_image` | body | `string` | yes | Base64-encoded hand signature image to apply when bulk signing. |
