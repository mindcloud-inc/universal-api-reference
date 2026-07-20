# Update Action with OnePageCRM

Updates an existing action in OnePageCRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/actions/:action_id`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [Update Action](https://developer.onepagecrm.com/api/#/Actions/put_actions__action_id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action_id` | path | `string` | yes | Action ID. |
| `done` | query | `boolean` | no | Mark the action as complete. |
| `contact_id` | body | `string` | no | ID of the contact associated with the action. |
| `text` | body | `string` | no | The main text or description of the action. Maximum length: 140. |
| `status` | body | `list<string>` | no | Status of the action. Accepted values: `asap`, `date`, `date_time`, `done`, `queued`, `queued_with_date`, `waiting`. |
| `date` | body | `string` | no | Due date for the action in YYYY-MM-DD format. |
| `exact_time` | body | `date` | no | UNIX epoch time in seconds when the action is due. |
| `assignee_id` | body | `string` | no | ID of the user assigned to the action. |
| `position` | body | `number` | no | Position of the action in the queued actions list. |
