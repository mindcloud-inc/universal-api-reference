# Update Member with WEBLUCY

Updates an existing member in WEBLUCY.

## Endpoint

- **Method:** `PUT`
- **Path:** `/members/{id}`
- **Base URL:** `https://apps.weblucy.com/api/site`
- **Official documentation:** [Update Member](https://websitebuilder.docs.apiary.io/#reference/members/single-member/update-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `approved` | body | `boolean` | no | Whether the member is approved. |
| `id` | path | `string` | yes | The member ID. |
| `name` | body | `string` | no | The member name. |
