# Create Person Contact with Clio Manage

Creates a new person contact in Clio Manage.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [Create Person Contact](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Contacts/operation/Contact%23create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.first_name` | body | `string` | yes |
| `data.last_name` | body | `string` | no |
