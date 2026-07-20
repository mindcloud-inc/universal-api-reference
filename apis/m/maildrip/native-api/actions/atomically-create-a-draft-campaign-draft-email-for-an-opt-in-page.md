# Atomically create a draft campaign + draft email for an opt-in page with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/opt-in-pages/{pageId}/quick-campaign`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Atomically create a draft campaign + draft email for an opt-in page](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `pageId` | path | `string` | yes |
| `campaign_name` | body | `string` | yes |
| `email_subject` | body | `string` | no |
