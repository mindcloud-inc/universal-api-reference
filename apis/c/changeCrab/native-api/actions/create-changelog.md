# Create Changelog with ChangeCrab

Creates a new changelog in ChangeCrab.

## Endpoint

- **Method:** `POST`
- **Path:** `/changelogs`
- **Base URL:** `https://changecrab.com/api`
- **Official documentation:** [Create Changelog](https://changecrab.com/knowledge-base/integrations/api-create-changelog)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The public name shown for the changelog. |
| `team` | body | `number` | yes | The owning ChangeCrab team ID. |
| `subdomain` | body | `string` | no | The changelog subdomain slug. |
| `siteurl` | body | `string` | no | The full website URL for the changelog. |
