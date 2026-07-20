# Add List Field with SendMails

Adds a custom field to a list in SendMails.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:uid/add-field`
- **Base URL:** `https://app.sendmails.io/api/v1`
- **Official documentation:** [Add List Field](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#3-toc-title)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | List UID from SendMails. |
| `type` | query | `string` | yes | Custom-field type: text, number, or datetime. |
| `label` | query | `string` | yes | Field label. |
| `tag` | query | `string` | yes | Field tag name using alphanumeric characters, dashes, or underscores. |
| `default_value` | query | `string` | no | Optional default value for the custom field. |
