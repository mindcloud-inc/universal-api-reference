# Add Signature Request Signer with Yousign

Creates a signer for a Yousign signature request.

## Endpoint

- **Method:** `POST`
- **Path:** `/signature_requests/:signatureRequestId/signers`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [Add Signature Request Signer](https://developers.yousign.com/reference/post-signature_requests-signaturerequestid-signers-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The Yousign signature request ID. |
| `contact_id` | body | `string` | yes | Existing contact to add as signer. |
| `signature_level` | body | `string` | yes | Signer signature level. |
| `signature_authentication_mode` | body | `string` | no | Signer authentication mode. |
| `delivery_mode` | body | `string` | no | Signer delivery mode. |
| `insert_after_id` | body | `string` | no | Recipient ID this signer should follow. |
| `group_with_id` | body | `string` | no | Recipient ID to group with. |
| `redirect_urls.success` | body | `string` | no | Redirect URL on successful signature. |
| `redirect_urls.error` | body | `string` | no | Redirect URL on signature error. |
| `redirect_urls.decline` | body | `string` | no | Redirect URL on signature decline. |
| `identification_attestation_id` | body | `string` | no | Identification attestation ID, when required. |
| `pre_identity_verification_required` | body | `boolean` | no | Require identity verification before signing. |
