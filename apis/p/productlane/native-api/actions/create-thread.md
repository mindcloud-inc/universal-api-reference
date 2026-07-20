# Create Thread with Productlane

Creates a new thread in Productlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/threads`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Create Thread](https://productlane.mintlify.dev/docs/api/threads/create-thread)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `text` | body | `string` | yes |
| `painLevel` | body | `string` | yes |
| `contactEmail` | body | `string` | yes |
| `title` | body | `string` | no |
| `state` | body | `string` | no |
| `origin` | body | `string` | no |
| `contactName` | body | `string` | no |
| `assigneeId` | body | `string` | no |
| `projectId` | body | `string` | no |
| `issueId` | body | `string` | no |
| `companyId` | body | `string` | no |
| `createdAt` | body | `date` | no |
| `updatedAt` | body | `date` | no |
| `notify` | body | `object` | no |
