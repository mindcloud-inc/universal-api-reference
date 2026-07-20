# Create Email Campaign with Go4Clients

Creates a new email campaign in Go4Clients.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/campaigns/email/v1.0/`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Create Email Campaign](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name set to the campaign. |
| `fromName` | body | `string` | yes | From name associated to the campaign sender email. |
| `fromEmail` | body | `string` | yes | From email of the campaign. |
| `replyEmail` | body | `string` | yes | Email address recipients reply to. |
| `subject` | body | `string` | yes | Subject used on the email campaign. |
| `template` | body | `object` | yes | Template object used on the campaign, for example {"body":"<html>...</html>"}. |
