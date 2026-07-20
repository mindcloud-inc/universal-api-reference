# Create Agreement Link with Harbour

Creates a new agreement link in Harbour.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.harbourshare.com/v1/agreement_links`
- **Base URL:** `https://api.myharbourshare.com/v2`
- **Official documentation:** [Create Agreement Link](https://developers.harbourshare.com/#create-agreement-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agreement_id` | query | `string` | yes | Agreement template identifier used to create the link. |
| `brand_id` | body | `string` | no | Brand identifier for the agreement link. |
| `request_title` | body | `string` | no | Title shown in the Harbour signature page. |
| `destination_folder_id` | body | `string` | yes | Folder where the completed agreement will be saved. |
| `auth_mode` | body | `string` | no | Authentication mode: PASSCODE, EMAILS, or PUBLIC. |
| `passcode` | body | `string` | no | Passcode value when auth_mode is PASSCODE. |
| `recipients[]` | body | `array<object>` | no | Array of recipient objects when auth_mode is EMAILS. |
| `is_active` | body | `boolean` | no | Whether the generated agreement link is active. |
