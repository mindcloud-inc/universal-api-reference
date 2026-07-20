# Create Community Member with Circle

Creates a new community member in Circle.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/v2/community_members`
- **Base URL:** `https://{subdomain}.circle.so`
- **Official documentation:** [Create Community Member](https://api.circle.so/apis/admin-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email of the community member |
| `skip_invitation` | body | `boolean` | no | Skip sending invitation email |
