# Get Outbound SMS Message Logs with Infobip

## Endpoint

- **Method:** `GET`
- **Path:** `/sms/3/logs`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Get Outbound SMS Message Logs](https://www.infobip.com/docs/api/channels/sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mcc` | query | `string` | no | Mobile Country Code. |
| `mnc` | query | `string` | no | Mobile Network Code. Mobile Country Code is required if this property is used. |
| `sender` | query | `string` | no | The sender ID which can be alphanumeric or numeric. |
| `destination` | query | `string` | no | Message destination address. |
| `bulkId` | query | `list<string>` | no | Unique ID assigned to the request if messaging multiple recipients or sending multiple messages via a single API request. May contain multiple comma-separated values. Maximum length 2048 characters. |
| `messageId` | query | `list<string>` | no | Unique message ID for which a log is requested. May contain multiple comma-separated values. Maximum length 2048 characters. |
| `generalStatus` | query | `string` | no | — |
| `sentSince` | query | `date` | no | The logs will only include messages sent after this date. Use it alongside sentUntil to specify a time range for the logs, but only up to the maximum limit of 1000 logs per call. Has the following format: yyyy-MM-dd'T'HH:mm:ss.SSSZ. |
| `sentUntil` | query | `date` | no | The logs will only include messages sent before this date. Use it alongside sentSince to specify a time range for the logs, but only up to the maximum limit of 1000 logs per call. Has the following format: yyyy-MM-dd'T'HH:mm:ss.SSSZ. |
| `limit` | query | `number` | no | Maximum number of messages to include in logs. If not set, the latest 50 records are returned. Maximum limit value is 1000 and you can only access logs for the last 48h. |
| `entityId` | query | `string` | no | Entity id used to send the message. For more details, see our [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `applicationId` | query | `string` | no | Application id used to send the message. For more details, see our [documentation](https://www.infobip.com/docs/cpaas-x/application-and-entity-management). |
| `campaignReferenceId` | query | `list<string>` | no | ID of a campaign that was sent in the message. May contain multiple comma-separated values. |
| `useCursor` | query | `boolean` | no | Flag used to enable cursor-based pagination. When set to true, the system will use the cursor to fetch the next set of logs. |
| `cursor` | query | `string` | no | Value which represents the current position in the data set. For the first request, this field shouldn't be defined. In subsequent requests, use the `nextCursor` value returned from the previous response to continue fetching data. |
