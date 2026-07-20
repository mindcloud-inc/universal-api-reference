# List Job Statuses with Aspire

Retrieves job statuses from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `JobStatuses`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Job Statuses](https://cloud-api.youraspire.com/swagger/index.html#/JobStatuses/JobStatuses_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
