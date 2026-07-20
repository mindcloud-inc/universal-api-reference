# Create Member Tag with Circle

Creates a new member tag in Circle.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/v2/member_tags`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Create Member Tag](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Member tag name |
| `display_format` | body | `list<string>` | yes | Display format for the member tag (label or icon) Accepted values: `icon`, `label`. |
