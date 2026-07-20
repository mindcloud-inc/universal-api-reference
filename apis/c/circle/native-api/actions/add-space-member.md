# Add Space Member with Circle

Creates a new space membership in Circle.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/v2/space_members`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Add Space Member](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to add to the space |
| `space_id` | body | `list<number>` | yes | Target space ID |
