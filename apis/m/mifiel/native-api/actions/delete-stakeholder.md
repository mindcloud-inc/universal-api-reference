# Delete Stakeholder with Mifiel

Deletes a stakeholder from a document in Mifiel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/documents/:documentId/stakeholders/:id`
- **Base URL:** `https://app.mifiel.com`
- **Official documentation:** [Delete Stakeholder](https://docs.mifiel.com/en/#tag/Stakeholders/operation/DeleteStakeholder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | Document ID. |
| `id` | path | `string` | yes | Stakeholder ID. |
