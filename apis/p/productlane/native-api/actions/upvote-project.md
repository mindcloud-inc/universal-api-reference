# Upvote Project with Productlane

Creates a project upvote in the Productlane portal.

## Endpoint

- **Method:** `POST`
- **Path:** `/portal/upvotes`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Upvote Project](https://productlane.mintlify.dev/docs/api/portal/upvote-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | End-user email for the upvote. |
| `issueId` | body | `string` | no | Issue ID to upvote. |
| `projectId` | body | `string` | no | Project ID to upvote. |
