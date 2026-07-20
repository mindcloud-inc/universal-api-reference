# Create Page Test with Calibre

Creates a new page test in Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Create Page Test](https://calibreapp.com/docs/automation/single-page-tests#create-a-page-test)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.url` | body | `string` | yes |
| `variables.location` | body | `string` | yes |
| `variables.device` | body | `string` | no |
| `variables.connection` | body | `string` | no |
| `variables.adBlockerIsEnabled` | body | `boolean` | no |
| `variables.isPrivate` | body | `boolean` | no |
| `variables.expiresAt` | body | `date` | no |
