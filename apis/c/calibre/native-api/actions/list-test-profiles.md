# List Test Profiles with Calibre

Retrieves test profiles for a site from Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [List Test Profiles](https://calibreapp.com/docs/automation/test-profiles#list-test-profiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.site` | body | `string` | yes | Site slug, found in site settings. |
