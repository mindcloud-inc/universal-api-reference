# Get New Hire Packet by ID with BambooHR

Retrieves new hire packet by id from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/new-hire-packets/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get New Hire Packet by ID](https://documentation.bamboohr.com/reference/9e50205e7d1577fae12f069776d705f7)

## Requirements

- **OAuth scopes:** `onboarding`
- **scope:** `onboarding` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
