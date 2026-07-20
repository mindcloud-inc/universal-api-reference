# Create Workflow with Twenty

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/workflows`
- **Base URL:** `https://api.twenty.com`
- **Official documentation:** [Create Workflow](https://docs.twenty.com/developers/extend/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lastPublishedVersionId` | body | `string` | no |
| `statuses[]` | body | `array<string>` | no |
| `name` | body | `string` | no |
