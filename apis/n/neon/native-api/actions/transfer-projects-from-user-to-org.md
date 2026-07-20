# Transfer projects from personal account to organization with Neon

Transfers projects to an organization in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/me/projects/transfer`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Transfer projects from personal account to organization](https://api-docs.neon.tech/reference/transferprojectsfromusertoorg)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination_org_id` | body | `string` | yes | Neon API parameter destination_org_id |
| `project_ids[]` | body | `array<string>` | yes | Neon API parameter project_ids |
