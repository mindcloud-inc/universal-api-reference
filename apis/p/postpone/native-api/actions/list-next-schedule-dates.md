# List Next Schedule Dates with Postpone

Retrieves next scheduled post dates from Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [List Next Schedule Dates](https://developers.postpone.app/examples/example-queries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.socialAccountIds[]` | body | `array<string>` | no | Optional list of social account IDs to filter schedule dates for. |
