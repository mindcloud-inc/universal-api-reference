# Create Site User with Voog

Creates a new site user for protected pages in Voog.

## Endpoint

- **Method:** `POST`
- **Path:** `/site_users`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Create Site User](https://www.voog.com/developers/api/resources/site_users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to invite as a site user. |
