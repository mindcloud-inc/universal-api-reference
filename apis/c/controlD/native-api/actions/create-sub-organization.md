# Create Sub-Organization with Control D

Creates a sub-organization in Control D.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/suborg`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Create Sub-Organization](https://docs.controld.com/reference/post_organizations-suborg)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | (Required) Organization name |
| `contact_email` | body | `string` | yes | Primary contact email for this sub-organization. |
| `twofa_req` | body | `number` | yes | Whether 2FA/MFA is required for members of this organization. 0 = no, 1 = yes. |
| `stats_endpoint` | body | `string` | yes | Primary key of the desired storage region. See List Storage Regions. |
| `address` | body | `string` | no | Physical address of this organization. |
| `website` | body | `string` | no | Website URL of this organization. |
| `contact_name` | body | `string` | no | Contact name for the person responsible for this organization. |
| `contact_phone` | body | `string` | no | Phone number associated with this organization. |
| `parent_profile` | body | `string` | no | Global profile ID to enforce on all created devices. |
