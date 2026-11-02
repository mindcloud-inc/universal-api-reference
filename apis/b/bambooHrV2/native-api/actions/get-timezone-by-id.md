# Get Timezone by ID with BambooHR

Retrieves timezone by id from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/meta/timezones/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Timezone by ID](https://documentation.bamboohr.com/reference/baa7162824294d030115568d1d8e6ca7)

## Requirements

- **OAuth scopes:** `meta`
- **scope:** `meta` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The numeric ID of the timezone to retrieve. |
