# Create Evidence With File Upload with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/entities/:entity_id/evidence`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Create Evidence With File Upload](https://column.com/docs/api/#entity/create-evidence-with-upload)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_id` | path | `string` | yes | — |
| `file` | body | `file` | yes | — |
| `purpose` | body | `list` | yes | Accepted values: `Active Status Certificate`, `Adverse Media Screening`, `Attestation Account Info Truth`, `Attestation Beneficial Ownership`, `Attestation Control Person`, `Attestation Privacy Policy`, `Attestation Terms of Service`, `Business Formation`, `Complete Customer File`, `EDD`, `IRS Form 990`, `IRS Form SS4`, `Identity Verification`, `Nonprofit Other Evidence`, `OFAC Screening`, `PEP Screening`, `Proof of Address`, `Signed Account Agreement`, `Tax ID Confirmation`. |
| `document_type` | body | `string` | yes | — |
| `description` | body | `string` | no | — |
