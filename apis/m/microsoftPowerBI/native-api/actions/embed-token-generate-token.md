# Generate Token with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `GenerateToken`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Generate Token](https://learn.microsoft.com/en-us/rest/api/power-bi/embed-token/generate-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasets[]` | body | `array<object>` | no | A list of datasets |
| `datasourceIdentities[]` | body | `array<object>` | no | List of identities to use when connecting to data sources with Single Sign-On (SSO) enabled. |
| `identities[]` | body | `array<object>` | no | The list of identities to use for row-level security rules |
| `lifetimeInMinutes` | body | `number` | no | The maximum lifetime of the token in minutes, starting from the time it was generated. Can be used to shorten the token's expiration time, but not to extend it. The value must be a positive integer. Zero (0) is equivalent to null, and will set the default expiration time. |
| `reports[]` | body | `array<object>` | no | A list of reports |
| `targetWorkspaces[]` | body | `array<object>` | no | The list of workspaces that the embed token will allow saving to |
