# Get Person Deletion Status with Rollbar

Retrieves person deletion status from Rollbar.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/delete_jobs/:jobId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Get Person Deletion Status](https://docs.rollbar.com/reference/get-person-deletion-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `number` | yes | Person deletion job identifier |
