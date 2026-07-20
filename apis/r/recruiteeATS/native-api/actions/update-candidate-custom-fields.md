# Update Candidate Custom Fields with Recruitee ATS

## Endpoint

- **Method:** `POST`
- **Path:** `/c/:company_id/custom_fields/candidates/:id/fields`
- **Base URL:** `https://api.recruitee.com`
- **Official documentation:** [Update Candidate Custom Fields](https://docs.recruitee.com/reference/custom_fieldscandidatesidfields-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Candidate ID. |
| `field.name` | body | `string` | yes | Profile field name. |
| `field.kind` | body | `string` | yes | Profile field kind. |
| `field.values` | body | `list<object>` | yes | Array of profile field value objects. |
