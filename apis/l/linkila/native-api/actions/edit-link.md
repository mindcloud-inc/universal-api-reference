# Edit Link with Linkila

Updates an existing link in Linkila.

## Endpoint

- **Method:** `POST`
- **Path:** `/editLink/:link_id`
- **Base URL:** `https://app.linkila.com/integrations/api/v1`
- **Official documentation:** [Edit Link](https://app.linkila.com/integrations/api/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `link_id` | path | `string` | yes | Required Linkila link identifier from the editLink path. |
| `changes` | body | `object` | no | Object containing the Linkila link fields to update. |
