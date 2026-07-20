# Update User with EducateMe

Updates an existing user in EducateMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:email`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [Update User](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#2c3447e2efaa80b39a46e8ef1561e687)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Existing user email. |
| `email` | body | `string` | no | Optional new email to update to. |
| `tagNamesToConnect[]` | body | `array<string>` | no | Tag names to connect. |
| `tagNamesToDisconnect[]` | body | `array<string>` | no | Tag names to disconnect. |
| `customProperties[]` | body | `array<object>` | no | Optional custom properties. |
