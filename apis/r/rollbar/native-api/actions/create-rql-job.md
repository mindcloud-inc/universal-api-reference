# Create RQL Job with Rollbar

Creates a new RQL job in Rollbar.

## Endpoint

- **Method:** `POST`
- **Path:** `/rql/jobs/`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Create RQL Job](https://docs.rollbar.com/reference/create-an-rql-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query_string` | body | `string` | yes | RQL query string to execute |
