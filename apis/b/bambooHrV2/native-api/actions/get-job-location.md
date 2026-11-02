# Get Job Location with BambooHR

Retrieves job location from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/hris/org/locations/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Job Location](https://documentation.bamboohr.com/reference/get-location)

## Requirements

- **OAuth scopes:** `field`
- **scope:** `field` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the location |
| `expand` | query | `list<string>` | no | Comma-separated list of related resources to expand. Supported values: state, country. Example: expand=state,country Accepted values: `country`, `state`. Send multiple values as a string separated by `,`. |
