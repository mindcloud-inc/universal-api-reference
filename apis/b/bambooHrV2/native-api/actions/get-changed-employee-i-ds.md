# Get Changed Employee I Ds with BambooHR

Retrieves changed employee i ds from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employees/changed`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Changed Employee I Ds](https://documentation.bamboohr.com/reference/get-changed-employee-ids)

## Requirements

- **OAuth scopes:** `public.integration public.user`
- **scope:** `public.integration, public.user` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since` | query | `date` | yes | ISO 8601 timestamp (URL-encoded). Only employees changed since this timestamp will be returned. |
| `type` | query | `list<string>` | no | Filter by change type. If omitted, all change types are returned. Accepted values: `all`, `deleted`, `inserted`, `updated`. |
