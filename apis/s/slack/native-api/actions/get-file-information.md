# Get File Information with Slack

Retrieves file details from a Slack workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `files.info`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Get File Information](https://docs.slack.dev/reference/methods/files.info/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | query | `list` | yes | Channel containing the file. |
| `file` | query | `list` | yes | ID of the file. |
