# Get Automation Subscriber Activity with MailerLite

Retrieves subscriber activity for an automation in MailerLite.

## Endpoint

- **Method:** `GET`
- **Path:** `/automations/:automationId/activity`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Get Automation Subscriber Activity](https://developers.mailerlite.com/docs/automations#get-the-subscriber-activity-for-an-automation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `automationId` | path | `string` | yes | MailerLite automation ID. |
| `filter[status]` | query | `string` | yes | Activity status: completed, active, canceled, or failed. |
| `filter[date_from]` | query | `date` | no | Start date for completed, canceled, or failed activity. |
| `filter[date_to]` | query | `date` | no | End date for completed, canceled, or failed activity. |
| `filter[scheduled_from]` | query | `date` | no | Start date for active scheduled activity. |
| `filter[scheduled_to]` | query | `date` | no | End date for active scheduled activity. |
| `filter[search]` | query | `string` | no | Filter activity by subscriber email address. |
| `limit` | query | `number` | no | Number of activity rows to return per page. |
| `page` | query | `number` | no | Page number to return. |
