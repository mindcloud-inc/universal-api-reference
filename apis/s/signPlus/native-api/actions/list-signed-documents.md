# List Signed Documents with Sign.Plus

## Endpoint

- **Method:** `GET`
- **Path:** `/envelope/:envelope_id/signed_documents`
- **Base URL:** `https://restapi.sign.plus/v2`
- **Official documentation:** [List Signed Documents](https://apidoc.sign.plus/api-reference/endpoints/signplus/get-envelope-signed_documents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes |
| `certificate_of_completion` | query | `boolean` | no |
