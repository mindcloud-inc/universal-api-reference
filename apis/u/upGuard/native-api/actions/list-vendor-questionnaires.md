# List Vendor Questionnaires with UpGuard

Retrieves vendor questionnaires from your UpGuard account.

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/questionnaires/v2`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Vendor Questionnaires](https://cyber-risk.upguard.com/api/docs#operation/questionnairesV2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exclude_archived` | query | `string` | no | Exclude archived questionnaires from the results. |
| `usage_type` | query | `string` | no | The usage type of questionnaires to return. |
| `vendor_id` | query | `string` | no | The ID of the vendor whose questionnaires should be listed. |
| `vendor_primary_hostname` | query | `string` | no | The primary hostname of the vendor whose questionnaires should be listed. |
