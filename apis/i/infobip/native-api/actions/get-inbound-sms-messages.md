# Get Inbound SMS Messages with Infobip

## Endpoint

- **Method:** `GET`
- **Path:** `/sms/1/inbox/reports`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Get Inbound SMS Messages](https://www.infobip.com/docs/api/channels/sms/inbound-sms/get-inbound-sms-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of messages to be returned in a response. If not set, the latest 50 records are returned. Maximum limit value is `1000` and you can only access messages for the last 48h. |
| `applicationId` | query | `string` | no | Application id that the message is linked to. For more details, see our [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `entityId` | query | `string` | no | Entity id that the message is linked to. For more details, see our [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `campaignReferenceId` | query | `string` | no | ID of a campaign that was sent in the message. |
