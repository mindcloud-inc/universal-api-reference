# Add Organization Stakeholder with CoordinateHQ

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationId/stakeholders`
- **Base URL:** `https://app.coordinatehq.com/api/v1`
- **Official documentation:** [Add Organization Stakeholder](https://app.coordinatehq.com/static/API_Documentation.html#organizations)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `stakeholder_email_address` | body | `string` | no |
