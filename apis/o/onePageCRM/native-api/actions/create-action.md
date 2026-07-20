# Create Action with OnePageCRM

Creates a new action in OnePageCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [Create Action](https://developer.onepagecrm.com/api/#/Actions/post_actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `string` | no | ID of the contact associated with the action. |
| `text` | body | `string` | no | The main text or description of the action. Maximum length: 140. |
| `status` | body | `list<string>` | no | Status of the action. Accepted values: `asap`, `date`, `date_time`, `done`, `queued`, `queued_with_date`, `waiting`. |
| `date` | body | `string` | no | Due date for the action in YYYY-MM-DD format. |
| `exact_time` | body | `date` | no | UNIX epoch time in seconds when the action is due. |
| `assignee_id` | body | `string` | no | ID of the user assigned to the action. |
| `position` | body | `number` | no | Position of the action in the queued actions list. |
