# Create Company Find Job with profileAPI

Creates a company search job in profileAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/find/jobs`
- **Base URL:** `https://api.profileapi.com/2024-03-01`
- **Official documentation:** [Create Company Find Job](https://documentation.profileapi.com/api-reference/create-company-find-job/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | yes | Filter groups containing all/any filter arrays for the company find job. |
| `limit` | body | `number` | no | Maximum number of matching companies for the background job when supported by provider filters. |
