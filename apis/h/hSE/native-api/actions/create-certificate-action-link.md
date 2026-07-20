# Create Certificate Action Link with 4HSE

Creates a new certificate-action link in 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/certificate-action/create`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Create Certificate Action Link](https://docs.4hse.com/en/api/certificateaction/#operation-createCertificateAction-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `certificate_id` | body | `string` | yes | The certificate being linked. |
| `action_id` | body | `string` | yes | The action the certificate is linked to. |
| `date_expire` | body | `date` | no | Expiration date specific to this link. |
| `tenant_id` | body | `string` | yes | The project this link belongs to. |
