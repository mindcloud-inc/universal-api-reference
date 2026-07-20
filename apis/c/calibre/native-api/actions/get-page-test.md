# Get Page Test with Calibre

Retrieves a page test by UUID from Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Get Page Test](https://calibreapp.com/docs/automation/single-page-tests#view-an-existing-test)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.uuid` | body | `string` | yes |
