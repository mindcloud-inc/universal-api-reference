# Update Batch Status with Certs 365

Updates batch certificate statuses in Certs 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/update-batch-status`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Update Batch Status](https://help.certs365.io/documentation/code-module-apis/revoke-reactivate-certification-batch/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Issuer email. |
| `batch` | body | `number` | yes | Certificate batch number. |
| `status` | body | `number` | yes | Batch status value. |
