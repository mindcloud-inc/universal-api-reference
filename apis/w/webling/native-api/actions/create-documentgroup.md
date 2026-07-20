# Create Documentgroup with Webling

## Endpoint

- **Method:** `POST`
- **Path:** `/documentgroup`
- **Base URL:** `https://{instanceDomain}/api/1`
- **Official documentation:** [Create Documentgroup](https://demo.webling.ch/api/1#documentgroup-documentgroup-list-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties.title` | body | `string` | yes | Title for the new document group. |
| `parents` | body | `number` | yes | Documentgroup ID that should own the new document group. |
