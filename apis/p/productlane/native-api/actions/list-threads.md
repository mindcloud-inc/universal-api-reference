# List Threads with Productlane

Retrieves threads from your Productlane workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/threads`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [List Threads](https://productlane.mintlify.dev/docs/api/threads/list-threads)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `state` | query | `string` | no |
| `issueId` | query | `string` | no |
| `projectId` | query | `string` | no |
