# Create Certificate with 4HSE

Creates a new certificate in 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/certificate/create`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Create Certificate](https://docs.4hse.com/en/api/certificate/#operation-createCertificate-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_release` | body | `date` | yes | Issue date of the certificate. |
| `date_expire` | body | `date` | no | Expiration date of the certificate. |
| `name` | body | `string` | yes | Descriptive name of the certificate. |
| `note` | body | `string` | no | Free-text notes. |
| `action_type` | body | `string` | yes | The type of requirement this certificate relates to. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `resource_id` | body | `string` | yes | The resource this certificate is issued to. |
| `tenant_id` | body | `string` | yes | The project this certificate belongs to. |
| `validity_unit` | body | `string` | no | Unit for the certificate validity period. Accepted values: `0`, `1`, `2`. |
| `validity` | body | `number` | no | Number of validity units. |
