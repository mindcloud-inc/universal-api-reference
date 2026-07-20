# Get Approval Comments with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.jodoo.com/api/v1/app/:app_id/entry/:entry_id/data/:data_id/approval_comments`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Get Approval Comments](https://help.jodoo.com/en/articles/9992419-approval-comments-query-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | Jodoo app ID that owns the workflow form. |
| `entry_id` | path | `string` | yes | Jodoo workflow form ID. |
| `data_id` | path | `string` | yes | Workflow form record ID. |
| `skip` | body | `number` | no | Number of approval comments to skip. |
