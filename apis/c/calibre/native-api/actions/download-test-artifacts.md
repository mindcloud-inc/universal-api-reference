# Download Test Artifacts with Calibre

Retrieves artifact download URLs for a page test from Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Download Test Artifacts](https://calibreapp.com/docs/automation/single-page-tests#retrieve-test-artifacts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.uuid` | body | `string` | yes |
| `variables.artifactName` | body | `string` | yes |
| `variables.mediaName` | body | `string` | yes |
