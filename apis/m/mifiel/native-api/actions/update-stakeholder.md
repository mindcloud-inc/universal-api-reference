# Update Stakeholder with Mifiel

Updates a stakeholder for a document in Mifiel.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/documents/:documentId/stakeholders/:id`
- **Base URL:** `https://app.mifiel.com`
- **Official documentation:** [Update Stakeholder](https://docs.mifiel.com/en/#tag/Stakeholders/operation/UpdateStakeholder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | Document ID. |
| `id` | path | `string` | yes | Stakeholder ID. |
| `email` | body | `string` | yes | Stakeholder email address. |
| `name` | body | `string` | no | Stakeholder full name. |
| `tax_id` | body | `string` | no | Tax ID (RFC in Mexico). |
| `send_invite` | body | `boolean` | no | Whether to send invitation emails automatically. |
| `type` | body | `string` | yes | Type of stakeholder: signer or reviewer. |
| `allowed_signature_methods[]` | body | `array<string>` | no | Allowed signature methods: FEA, FESCV, or FESSV. |
