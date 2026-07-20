# Create Inbox Lead with Clio Grow

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox_leads`
- **Base URL:** `https://api.clio.com/grow`
- **Official documentation:** [Create Inbox Lead](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Inbox-Leads/operation/InboxLead%23create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.first_name` | body | `string` | yes | First name of the lead. |
| `data.last_name` | body | `string` | yes | Last name of the lead. |
| `data.from_message` | body | `string` | yes | Message content from the lead. |
| `data.referring_url` | body | `string` | yes | URL the lead came from. |
| `data.from_source` | body | `string` | yes | Source of the lead. |
| `data.email` | body | `string` | no | Email address of the lead. |
| `data.phone_number` | body | `string` | no | Phone number of the lead. |
