# Create Domain with Release0

Creates a custom domain in Release0.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/domains`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [Create Domain](https://docs.release0.com/workspace/customDomains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | The domain to create. |
| `workspaceId` | body | `string` | yes | The workspace ID that owns the domain. |
