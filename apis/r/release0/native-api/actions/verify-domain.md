# Verify Domain with Release0

Checks whether a custom domain is verified in Release0.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/domains/:name/verify`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [Verify Domain](https://docs.release0.com/workspace/customDomains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The domain name to verify. |
| `workspaceId` | query | `string` | yes | The workspace that owns the domain to verify. |
