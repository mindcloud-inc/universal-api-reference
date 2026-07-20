# Set Current Status with Pachca (Admin)

Updates your current status in the Pachca Admin API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/profile/status`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Set Current Status](https://dev.pachca.com/api/profile/update-status)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `emoji` | body | `string` | yes |
| `title` | body | `string` | yes |
| `expires_at` | body | `date` | no |
| `is_away` | body | `boolean` | no |
| `away_message` | body | `string` | no |
