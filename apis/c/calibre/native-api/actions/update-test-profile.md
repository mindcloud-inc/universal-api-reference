# Update Test Profile with Calibre

Updates an existing test profile in Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Update Test Profile](https://calibreapp.com/docs/automation/test-profiles#update-a-test-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.site` | body | `string` | yes | Site slug, found in site settings. |
| `variables.uuid` | body | `string` | yes | UUID of the test profile to update. |
| `variables.name` | body | `string` | no | A descriptive name for the test profile. |
| `variables.device` | body | `string` | no | Device tag to emulate during tests. |
| `variables.connection` | body | `string` | no | Network throttling tag for the profile. |
| `variables.adBlockerIsEnabled` | body | `boolean` | no | Enable the ad blocker during tests. |
| `variables.jsIsDisabled` | body | `boolean` | no | Disable JavaScript requests during the test. |
| `variables.position` | body | `number` | no | Optional order position for the profile. |
