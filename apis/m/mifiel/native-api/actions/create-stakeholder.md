# Create Stakeholder with Mifiel

Creates a stakeholder for a document in Mifiel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/documents/:documentId/stakeholders`
- **Base URL:** `https://app.mifiel.com`
- **Official documentation:** [Create Stakeholder](https://docs.mifiel.com/en/#tag/Stakeholders/operation/CreateStakeholder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | Document ID. |
| `email` | body | `string` | yes | Stakeholder email address. |
| `name` | body | `string` | no | Stakeholder full name. |
| `tax_id` | body | `string` | no | Tax ID (RFC in Mexico). |
| `type` | body | `string` | yes | Type of stakeholder: signer or reviewer. |
