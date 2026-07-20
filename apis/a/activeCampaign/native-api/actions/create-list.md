# Create List with ActiveCampaign

Creates a new list in ActiveCampaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [Create List](https://developers.activecampaign.com/reference/create-new-list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `list` | body | `object` | no |
| `list.name` | body | `string` | yes |
| `list.stringid` | body | `string` | yes |
| `list.sender_url` | body | `string` | yes |
| `list.sender_reminder` | body | `string` | yes |
| `list.send_last_broadcast` | body | `boolean` | no |
| `list.carboncopy` | body | `string` | no |
| `list.subscription_notify` | body | `string` | no |
| `list.unsubscription_notify` | body | `string` | no |
| `list.user` | body | `number` | no |
| `list.channel` | body | `string` | no |
