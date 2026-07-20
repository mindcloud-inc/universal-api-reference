# List User Call Records with RingCentral

Returns call log records filtered by parameters specified.

## Endpoint

- **Method:** `GET`
- **Path:** `restapi/v1.0/account/:accountId/extension/:extensionId/call-log`
- **Base URL:** `https://platform.ringcentral.com/`
- **Official documentation:** [List User Call Records](https://developers.ringcentral.com/api-reference/Call-Log/readCompanyCallLog)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Internal identifier of the RingCentral account. Default value is "~" to indicate that the account associated with current authorization session should be used. |
| `extensionNumber` | query | `string` | no | Short extension number of a user. If specified, returns call log for this particular extension only.  Cannot be combined with `phoneNumber` filter |
| `direction` | query | `list<string>` | no | The direction of call records to be included in the result. If omitted, both inbound and outbound calls are returned. |
| `type` | query | `list<string>` | no | The type of call records to be included in the result. If omitted, all call types are returned. |
| `view` | query | `list<string>` | no | Defines the level of details for returned call records. |
| `withRecording` | query | `boolean` | no | Deprecated, replaced with `recordingType` filter, still supported for compatibility reasons. Indicates if only recorded calls should be returned.  If both `withRecording` and `recordingType` parameters are specified, then `withRecording` is ignored |
| `recordingType` | query | `list<string>` | no | Indicates that call records with recordings of particular type should be returned. If omitted, then calls with and without recordings are returned. |
| `dateFrom` | query | `string` | no | The beginning of the time range to return call records in ISO 8601 format including timezone, for example `2016-03-10T18:07:52.534Z`.  The default value is `dateTo` minus 24 hours |
| `dateTo` | query | `string` | no | The end of the time range to return call records in ISO 8601 format including timezone, for example `2016-03-10T18:07:52.534Z`.  The default value is current time. |
| `sessionId` | query | `string` | no | Internal identifier of a call session. |
| `telephonySessionId` | query | `string` | no | Internal identifier of a telephony session. |
| `metadataCategory` | query | `string` | no | Send multiple values as a array. |
| `showDeleted` | query | `boolean` | no | Indicates that deleted calls records should be returned |
| `extensionId` | path | `string` | yes | Internal identifier of the RingCentral extension. Default value is "~" to indicate that the extension associated with current authorization session should be used. |
