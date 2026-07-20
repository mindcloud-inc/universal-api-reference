# Get Award Project Outcomes with National Science Foundation

Retrieves a project outcomes report from National Science Foundation.

## Endpoint

- **Method:** `GET`
- **Path:** `/awards/[:id]/projectoutcomes.json`
- **Base URL:** `https://api.nsf.gov/services/v1`
- **Official documentation:** [Get Award Project Outcomes](https://resources.research.gov/common/webapi/awardapisearch-v1.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Award unique identifier whose project outcomes report should be retrieved, such as 1052893. |
