# Create Entry with Canny

Creates a new entry in Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/entries/create`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [Create Entry](https://developers.canny.io/api-reference#create_entry)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | yes |
| `details` | body | `string` | yes |
| `type` | body | `string` | no |
| `published` | body | `boolean` | no |
| `notify` | body | `boolean` | no |
| `publishedOn` | body | `date` | no |
| `scheduledFor` | body | `date` | no |
| `labelIDs` | body | `list<string>` | no |
| `postIDs` | body | `list<string>` | no |
