# Get Outbound SMS Delivery Reports with Infobip

## Endpoint

- **Method:** `GET`
- **Path:** `/sms/3/reports`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Get Outbound SMS Delivery Reports](https://www.infobip.com/docs/api/channels/sms/logs-and-status-reports/get-outbound-sms-message-delivery-reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulkId` | query | `string` | no | The ID that uniquely identifies the request. Bulk ID will be received only when you send a message to more than one destination address. |
| `messageId` | query | `string` | no | The ID that uniquely identifies the message sent. |
| `limit` | query | `number` | no | Maximum number of delivery reports to be returned. If not set, the latest 50 records are returned. Maximum limit value is 1000 and you can only access reports for the last 48h |
| `entityId` | query | `string` | no | Entity id used to send the message. For more details, see our [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `applicationId` | query | `string` | no | Application id used to send the message. For more details, see our [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `campaignReferenceId` | query | `string` | no | ID of a campaign that was sent in the message. |
