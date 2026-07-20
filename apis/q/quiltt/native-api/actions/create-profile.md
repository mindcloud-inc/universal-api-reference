# Create Profile with Quiltt

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/profiles`
- **Base URL:** `https://api.quiltt.io`
- **Official documentation:** [Create Profile](https://www.quiltt.dev/api/profiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Profile email address. |
| `name` | body | `string` | no | Profile display name. |
| `phone` | body | `string` | no | Profile phone number. |
| `uuid` | body | `string` | no | Optional custom UUID for the new profile. |
