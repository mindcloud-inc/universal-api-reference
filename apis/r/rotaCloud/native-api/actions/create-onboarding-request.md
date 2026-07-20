# Create Onboarding Request with RotaCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/users/onboard`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Create Onboarding Request](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locations[]` | body | `array<number>` | yes | Location IDs for onboarding. |
| `users[]` | body | `array<object>` | yes | Pending users to onboard. |
