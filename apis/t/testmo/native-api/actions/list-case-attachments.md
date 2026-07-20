# List Case Attachments with Testmo

Retrieves attachments for a test case in Testmo.

## Endpoint

- **Method:** `GET`
- **Path:** `/cases/{case_id}/attachments`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [List Case Attachments](https://support.testmo.com/hc/en-us/articles/40045804558093-Attachments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_id` | path | `number` | yes | ID of the case whose attachments should be listed. |
