# Change Alert Status with Chargback

Updates an existing alert status in Chargback.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/public/v1/alerts/:external_id/`
- **Base URL:** `https://api.chargeback.io`
- **Official documentation:** [Change Alert Status](https://api.chargeback.io/api/public/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `external_id` | path | `string` | yes |
| `status` | body | `string` | yes |
