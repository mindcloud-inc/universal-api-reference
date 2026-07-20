# Update Auth Preferences with Invidious

## Endpoint

- **Method:** `POST`
- **Path:** `/auth/preferences`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Update Auth Preferences](https://docs.invidious.io/api/authenticated-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `speed` | body | `number` | no | Playback speed preference. |
| `volume` | body | `number` | no | Volume preference. |
