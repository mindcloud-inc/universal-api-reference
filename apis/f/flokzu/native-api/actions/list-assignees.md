# List Assignees with Flokzu

## Endpoint

- **Method:** `GET`
- **Path:** `/commons/assignee/list`
- **Base URL:** `https://app.flokzu.com/flokzuopenapi/api`
- **Official documentation:** [List Assignees](https://flokzu.docs.apiary.io/reference/commons/assignees/get-assignee-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignees` | query | `string` | yes | JSON array string of email addresses and/or role names. |
