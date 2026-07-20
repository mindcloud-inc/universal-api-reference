# Cancel Ready Campaign with MailerLite

Cancels a ready campaign in MailerLite.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:campaignId/cancel`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Cancel Ready Campaign](https://developers.mailerlite.com/docs/campaigns#cancel-a-ready-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Ready campaign ID to cancel. |
