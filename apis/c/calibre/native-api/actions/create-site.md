# Create Site with Calibre

Creates a new site in Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Create Site](https://calibreapp.com/docs/automation/managing-sites#create-a-site)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.siteName` | body | `string` | yes | Name of the Calibre site to create. |
| `variables.team` | body | `string` | yes | Team slug that will own the new site. |
| `variables.location` | body | `string` | no | Primary test location for the new site. |
| `variables.canonicalUrl` | body | `string` | yes | Canonical URL for the site. |
| `variables.pageName` | body | `string` | no | Name of the initial page added to the site. |
