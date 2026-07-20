# Get Award with National Science Foundation

Retrieves award information from National Science Foundation by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/awards/[:id].json`
- **Base URL:** `https://api.nsf.gov/services/v1`
- **Official documentation:** [Get Award](https://resources.research.gov/common/webapi/awardapisearch-v1.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Award unique identifier, such as 1052893. |
