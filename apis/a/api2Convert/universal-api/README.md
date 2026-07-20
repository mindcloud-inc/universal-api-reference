# <img src="https://images.mindcloud.co/apps/icons/api2convert-icon_1776189402884.png" alt="Api2Convert logo" width="28" height="28"> Api2Convert: Universal API

File conversion API for creating conversion jobs, managing inputs, outputs, presets, contracts, statuses, and usage statistics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/api2Convert/latest
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.api2convert.com
- **Vendor API docs:** https://api.api2convert.com/v2/schema

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contracts](actions/get-contracts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-contracts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Contract

| Action | Method | Description |
| --- | --- | --- |
| [Get Contracts](actions/get-contracts.md) | GET | Retrieves active contract details from Api2Convert. |

### Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Conversion](actions/create-job-conversion.md) | POST | Creates a conversion for a job in Api2Convert. |
| [Delete Job Conversion](actions/delete-job-conversion.md) | DELETE | Deletes a job conversion from Api2Convert. |
| [Get Conversions](actions/get-conversions.md) | GET | Retrieves valid conversion types from Api2Convert. |
| [Get Job Conversion](actions/get-job-conversion.md) | GET | Retrieves a job conversion from Api2Convert. |
| [List Job Conversions](actions/list-job-conversions.md) | GET | Retrieves conversions for a job from Api2Convert. |
| [Update Job Conversion](actions/update-job-conversion.md) | PUT | Updates an existing job conversion in Api2Convert. |

### Daily Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Statistics](actions/get-daily-statistics.md) | GET | Retrieves statistics for a specific day from Api2Convert. |

### History Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Job History](actions/get-job-history.md) | GET | Retrieves change history for a job from Api2Convert. |

### Input File

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Input](actions/create-job-input.md) | POST | Creates an input file for a job in Api2Convert. |
| [Delete Job Input](actions/delete-job-input.md) | DELETE | Deletes an input file from a job in Api2Convert. |
| [Get Job Input](actions/get-job-input.md) | GET | Retrieves an input file from a job in Api2Convert. |
| [List Job Inputs](actions/list-job-inputs.md) | GET | Retrieves input files for a job from Api2Convert. |
| [Update Job Input](actions/update-job-input.md) | PUT | Updates an input file for a job in Api2Convert. |
| [Update Job Inputs](actions/update-job-inputs.md) | PUT | Updates input files for a job in Api2Convert. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST | Creates a new job in Api2Convert. |
| [Delete Job](actions/delete-job.md) | DELETE | Cancels an existing job in Api2Convert. |
| [Get Job](actions/get-job.md) | GET | Retrieves details for a job from Api2Convert. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves active job records from Api2Convert. |
| [Update Job](actions/update-job.md) | PUT | Updates an existing job in Api2Convert. |

### Monthly Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Monthly Statistics](actions/get-monthly-statistics.md) | GET | Retrieves statistics for a specific month from Api2Convert. |

### Output File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Job Output](actions/delete-job-output.md) | DELETE | Deletes an output file from a job in Api2Convert. |
| [Get Job Output](actions/get-job-output.md) | GET | Retrieves an output file from a job in Api2Convert. |
| [List Job Outputs](actions/list-job-outputs.md) | GET | Retrieves output files for a job from Api2Convert. |
| [Update Job Output](actions/update-job-output.md) | PUT | Updates an output file for a job in Api2Convert. |
| [Update Job Outputs](actions/update-job-outputs.md) | PUT | Updates output files for a job in Api2Convert. |

### Preset

| Action | Method | Description |
| --- | --- | --- |
| [Create Preset](actions/create-preset.md) | POST | Creates a new preset in Api2Convert. |
| [Delete Preset](actions/delete-preset.md) | DELETE | Deletes an existing preset from Api2Convert. |
| [Get Preset](actions/get-preset.md) | GET | Retrieves a specific preset from Api2Convert. |
| [List Presets](actions/list-presets.md) | GET | Retrieves available conversion presets from Api2Convert. |
| [Update Preset](actions/update-preset.md) | PUT | Updates an existing preset in Api2Convert. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Statuses](actions/get-statuses.md) | GET | Retrieves valid job statuses from Api2Convert. |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [List Job Threads](actions/list-job-threads.md) | GET | Retrieves processing threads for a job from Api2Convert. |

### Yearly Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Yearly Statistics](actions/get-yearly-statistics.md) | GET | Retrieves statistics for a specific year from Api2Convert. |

