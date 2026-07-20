# Refresh Authorization Token with Aspire

Refreshes the current authorization token in Aspire.

## Endpoint

- **Method:** `POST`
- **Path:** `Authorization/RefreshToken`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Refresh Authorization Token](https://cloud-api.youraspire.com/swagger/index.html#/Authorization/Authorization_RefreshToken)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `RefreshToken` | body | `string` | no |
