# Take Action on Violations with Nightfall.ai

Updates violations by applying actions in Nightfall.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/dlp/v1/violations/actions`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Take Action on Violations](https://help.nightfall.ai/developer-api/nightfall_apis/saas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `violationUUIDs[]` | body | `array<string>` | yes | Array of violation UUIDs to act on. |
| `action` | body | `string` | yes | The Nightfall action to perform on the supplied violations. |
