# Create Member with WEBLUCY

Creates a new member in WEBLUCY.

## Endpoint

- **Method:** `POST`
- **Path:** `/members`
- **Base URL:** `https://apps.weblucy.com/api/site`
- **Official documentation:** [Create Member](https://websitebuilder.docs.apiary.io/#reference/members/list-and-create/create-new-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The member email address. |
| `name` | body | `string` | yes | The member name. |
| `password` | body | `string` | yes | The member password. If omitted, WEBLUCY sends a password reset email instead. |
