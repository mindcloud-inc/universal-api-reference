# List Files with Slack

Retrieves files from a Slack workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `files.list`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [List Files](https://docs.slack.dev/reference/methods/files.list/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | query | `list<string>` | yes | Filter files appearing in a specific channel, indicated by its ID. |
| `show_files_hidden_by_limit` | query | `boolean` | no | Show truncated file info for files hidden due to being too old, and the team who owns the file being over the file limit Format: `toggle`. |
| `ts_from` | query | `date` | no | Filter files created after this timestamp (inclusive). |
| `ts_to` | query | `date` | no | Filter files created before this timestamp (inclusive). |
| `types` | query | `list<string>` | no | Filter files by type Send multiple values as a array. |
| `user` | query | `list<string>` | no | Filter files created by a single user. |
