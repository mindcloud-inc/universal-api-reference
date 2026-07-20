# Duplicate Campaign with SureContact

Creates a draft copy of a SureContact campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/public/campaigns/:campaign_uuid/duplicate`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Duplicate Campaign](https://api.surecontact.com/docs#endpoints-POSTapi-v1-public-campaigns--campaign_uuid--duplicate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaign_uuid` | path | `string` | yes |
| `name` | body | `string` | no |
