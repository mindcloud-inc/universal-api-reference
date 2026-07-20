# Api2Convert: Native API Reference

A consolidated summary of Api2Convert's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://api.api2convert.com/v2/schema
- **API base URL:** `https://api.api2convert.com/v2`

## Authentication

### API Key

Custom auth for Api2Convert using the provider-required X-Oc-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required · Api2Convert API key used in the X-Oc-Api-Key header for every request.

Send these headers with each API request:

```http
X-Oc-Api-Key: <apiKey>
```

[Official authentication documentation](https://api.api2convert.com/v2/schema)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `408,409,425,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | `POST /jobs` | [docs](https://api.api2convert.com/v2/schema) |
| [Create Job Conversion](actions/create-job-conversion.md) | `POST /jobs/:job_id/conversions` | [docs](https://api.api2convert.com/v2/schema) |
| [Create Job Input](actions/create-job-input.md) | `POST /jobs/:job_id/input` | [docs](https://api.api2convert.com/v2/schema) |
| [Create Preset](actions/create-preset.md) | `POST /presets` | [docs](https://api.api2convert.com/v2/schema) |
| [Delete Job](actions/delete-job.md) | `DELETE /jobs/:job_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Delete Job Conversion](actions/delete-job-conversion.md) | `DELETE /jobs/:job_id/conversions/:conversion_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Delete Job Input](actions/delete-job-input.md) | `DELETE /jobs/:job_id/input/:file_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Delete Job Output](actions/delete-job-output.md) | `DELETE /jobs/:job_id/output/:file_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Delete Preset](actions/delete-preset.md) | `DELETE /presets/:preset_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Get Contracts](actions/get-contracts.md) | `GET /contracts` | [docs](https://api.api2convert.com/v2/schema) |
| [Get Conversions](actions/get-conversions.md) | `GET /conversions` | [docs](https://api.api2convert.com/v2/schema) |
| [Get Daily Statistics](actions/get-daily-statistics.md) | `GET /stats/day/:day/:filter` | [docs](https://api.api2convert.com/v2/schema) |
| [Get Job](actions/get-job.md) | `GET /jobs/:job_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Get Job Conversion](actions/get-job-conversion.md) | `GET /jobs/:job_id/conversions/:conversion_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Get Job History](actions/get-job-history.md) | `GET /jobs/:job_id/history` | [docs](https://api.api2convert.com/v2/schema) |
| [Get Job Input](actions/get-job-input.md) | `GET /jobs/:job_id/input/:file_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Get Job Output](actions/get-job-output.md) | `GET /jobs/:job_id/output/:file_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Get Monthly Statistics](actions/get-monthly-statistics.md) | `GET /stats/month/:month/:filter` | [docs](https://api.api2convert.com/v2/schema) |
| [Get Preset](actions/get-preset.md) | `GET /presets/:preset_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Get Statuses](actions/get-statuses.md) | `GET /statuses` | [docs](https://api.api2convert.com/v2/schema) |
| [Get Yearly Statistics](actions/get-yearly-statistics.md) | `GET /stats/year/:year/:filter` | [docs](https://api.api2convert.com/v2/schema) |
| [List Job Conversions](actions/list-job-conversions.md) | `GET /jobs/:job_id/conversions` | [docs](https://api.api2convert.com/v2/schema) |
| [List Job Inputs](actions/list-job-inputs.md) | `GET /jobs/:job_id/input` | [docs](https://api.api2convert.com/v2/schema) |
| [List Job Outputs](actions/list-job-outputs.md) | `GET /jobs/:job_id/output` | [docs](https://api.api2convert.com/v2/schema) |
| [List Job Threads](actions/list-job-threads.md) | `GET /jobs/:job_id/threads` | [docs](https://api.api2convert.com/v2/schema) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://api.api2convert.com/v2/schema) |
| [List Presets](actions/list-presets.md) | `GET /presets` | [docs](https://api.api2convert.com/v2/schema) |
| [Update Job](actions/update-job.md) | `PATCH /jobs/:job_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Update Job Conversion](actions/update-job-conversion.md) | `PATCH /jobs/:job_id/conversions/:conversion_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Update Job Input](actions/update-job-input.md) | `PATCH /jobs/:job_id/input/:file_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Update Job Inputs](actions/update-job-inputs.md) | `PATCH /jobs/:job_id/input` | [docs](https://api.api2convert.com/v2/schema) |
| [Update Job Output](actions/update-job-output.md) | `PATCH /jobs/:job_id/output/:file_id` | [docs](https://api.api2convert.com/v2/schema) |
| [Update Job Outputs](actions/update-job-outputs.md) | `PATCH /jobs/:job_id/output` | [docs](https://api.api2convert.com/v2/schema) |
| [Update Preset](actions/update-preset.md) | `PATCH /presets/:preset_id` | [docs](https://api.api2convert.com/v2/schema) |
