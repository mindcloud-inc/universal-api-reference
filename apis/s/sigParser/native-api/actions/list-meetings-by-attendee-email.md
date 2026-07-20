# List Meetings By Attendee Email with SigParser

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Meetings/Distinct`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [List Meetings By Attendee Email](https://ipaas.sigparser.com/v1#get-api-meetings-distinct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailaddress` | query | `string` | yes | Attendee email address to filter by. |
