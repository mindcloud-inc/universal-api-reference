# Create Site with Collected Notes

## Endpoint

- **Method:** `POST`
- **Path:** `/sites`
- **Base URL:** `https://collectednotes.com`
- **Official documentation:** [Create Site](https://collectednotes.com/blog/api#create-a-site)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site` | body | `object` | no |
| `site.name` | body | `string` | yes |
| `site.site_path` | body | `string` | yes |
