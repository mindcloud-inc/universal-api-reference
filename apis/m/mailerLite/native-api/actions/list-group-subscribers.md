# List Group Subscribers with MailerLite

Retrieves subscribers from a specific group in MailerLite.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_id/subscribers`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [List Group Subscribers](https://developers.mailerlite.com/docs/groups#get-subscribers-belonging-to-a-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `string` | yes | Existing MailerLite group identifier. |
| `filter[status]` | query | `string` | no | Return subscribers with this status. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `limit` | query | `number` | no | Number of subscribers to return. |
| `cursor` | query | `string` | no | Pagination cursor from a previous response. |
| `include` | query | `string` | no | Additional resources to include in the response. Accepted values: `0`. |
