# Import Bulk Subscribers to Group with MailerLite

Imports multiple subscribers into a group in MailerLite.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:group_id/import-subscribers`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Import Bulk Subscribers to Group](https://developers.mailerlite.com/docs/groups#import-bulk-subscribers-to-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `string` | yes | Existing MailerLite group identifier. |
| `subscribers[]` | body | `array<object>` | yes | Array of subscriber objects to import into the group. |
