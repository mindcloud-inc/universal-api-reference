# Create Webhook with Salesforge

Creates a webhook in Salesforge.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v2/workspaces/:workspaceID/integrations/webhooks`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Create Webhook](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | — |
| `name` | body | `string` | yes | — |
| `type` | body | `list` | yes | Accepted values: `contact_unsubscribed`, `dnc_added`, `email_bounced`, `email_opened`, `email_replied`, `email_sent`, `label_changed`, `link_clicked`, `linkedin_replied`, `negative_reply`, `positive_reply`. |
| `url` | body | `string` | yes | — |
| `sequenceID` | body | `string` | no | — |
