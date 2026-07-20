# Update Mailing List with Direct Mail Manager

## Endpoint

- **Method:** `PUT`
- **Path:** `/mailing-lists/:mlg_lst_id`
- **Base URL:** `https://api.directmailmanager.com/api`
- **Official documentation:** [Update Mailing List](https://apidocs.directmailmanager.com/#tag/Mailing-Lists/operation/update-mailing-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mlg_lst_id` | path | `string` | yes | The unique ID of the mailing list. |
| `name` | body | `string` | no | The updated mailing list name. |
