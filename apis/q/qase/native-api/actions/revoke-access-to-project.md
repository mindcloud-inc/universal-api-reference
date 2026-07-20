# Revoke access to project by code with Qase

Revokes access to a project in Qase.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/project/:code/access`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Revoke access to project by code](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `member_id` | body | `number` | no | Member ID. |
