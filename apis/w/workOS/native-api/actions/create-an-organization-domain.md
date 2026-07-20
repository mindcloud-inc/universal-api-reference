# Create an Organization Domain with WorkOS

Creates an organization domain in your WorkOS environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/organization_domains`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Create an Organization Domain](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | The domain to add to the organization. |
| `organization_id` | body | `string` | yes | The ID of the organization to add the domain to. |
