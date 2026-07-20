# Update Test URL Settings with TestDome

Updates test URL settings in TestDome.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tests/:testId/url-settings`
- **Base URL:** `https://api.staging.testdome.com/v3`
- **Official documentation:** [Update Test URL Settings](https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `candidatesLimit` | body | `number` | no |
| `deadline` | body | `string` | no |
| `id` | path | `number` | yes |
| `proctoringEnabled` | body | `boolean` | no |
| `verifyCandidates` | body | `boolean` | no |
