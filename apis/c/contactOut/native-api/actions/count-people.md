# Count People with ContactOut

Retrieves a count of people matching search filters in ContactOut.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people/count`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Count People](https://api.contactout.com/#people-count-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | Filter by company. |
| `job_title` | body | `string` | no | Filter by job title. |
| `name` | body | `string` | no | Match people by name. |
