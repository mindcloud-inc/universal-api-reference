# Create Review Request with gotoHuman

Creates a new review request in gotoHuman.

## Endpoint

- **Method:** `POST`
- **Path:** `/requestReview`
- **Base URL:** `https://api.gotohuman.com`
- **Official documentation:** [Create Review Request](https://docs.gotohuman.com/send-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | body | `string` | yes | The ID of the review template / form. |
| `fields` | body | `string` | yes | JSON object of field values shaped by the selected review template. |
| `meta` | body | `string` | no | JSON object of additional metadata returned in the webhook. |
| `assignTo` | body | `string` | no | JSON array string of reviewer email addresses. |
| `assignToGroups` | body | `string` | no | JSON array string of reviewer group IDs. |
| `title` | body | `string` | no | Custom title displayed for the review request. |
| `webhookUrl` | body | `string` | no | Dynamic webhook URL for this request. |
| `autoApprove` | body | `boolean` | no | Automatically approve the review request. |
