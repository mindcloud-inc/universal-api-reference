# Get Contacts Based on Your Criteria with Dotdigital

Finds contacts in Dotdigital by selected criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/v3`
- **Base URL:** `https://r2-api.dotmailer.com`
- **Official documentation:** [Get Contacts Based on Your Criteria](https://developer.dotdigital.com/reference/getcontacts-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data-fields` | query | `string` | no | Pipe-delimited contact data field keys to return, or [[ALL]] to return all data fields. Send multiple values as a string separated by `\|`. |
| `include` | query | `list<string>` | no | Additional contact datasets to include in the response. Accepted values: `channelProperties`, `consentRecords`, `lists`, `preferences`. Send multiple values as a string separated by `\|`. |
| `~created` | query | `string` | no | Use gte::YYYY-MM-DDTHH:MM:SSZ to filter by created date. Do not use with Modified Filter. |
| `~modified` | query | `string` | no | Use gte::YYYY-MM-DDTHH:MM:SSZ to filter by modified date. |
| `~listId` | query | `number` | no | Filter to a specific list. Do not use with Segment ID Filter. |
| `~segmentId` | query | `number` | no | Filter to a specific segment. Do not use with List ID Filter. |
