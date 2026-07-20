# Create Document with Autype

Creates a new document in Autype.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://api.autype.com/api/v1/dev`
- **Official documentation:** [Create Document](https://docs.autype.com/api-reference/developer-api/create-document)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `content` | body | `object` | no |
| `description` | body | `string` | no |
| `projectId` | body | `string` | yes |
| `title` | body | `string` | yes |
