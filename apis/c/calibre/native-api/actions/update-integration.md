# Update Integration with Calibre

Updates an existing integration in Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Update Integration](https://calibreapp.com/docs/automation/integrations#update-integration)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.site` | body | `string` | yes |
| `variables.uuid` | body | `string` | yes |
| `variables.provider` | body | `string` | yes |
| `variables.url` | body | `string` | no |
| `variables.event` | body | `string<string>` | yes |
| `variables.secret` | body | `string` | no |
| `variables.isDisabled` | body | `boolean` | no |
