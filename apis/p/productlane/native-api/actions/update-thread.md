# Update Thread with Productlane

Updates an existing thread in Productlane.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/threads/:id`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Update Thread](https://productlane.mintlify.dev/docs/api/threads/update-thread)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `text` | body | `string` | no |
| `title` | body | `string` | no |
| `painLevel` | body | `string` | no |
| `assigneeId` | body | `string` | no |
| `projectId` | body | `string` | no |
| `notify` | body | `object` | no |
| `state` | body | `string` | no |
| `contactId` | body | `string` | no |
| `companyId` | body | `string` | no |
| `tagIds[]` | body | `array<string>` | no |
| `updatedAt` | body | `date` | no |
