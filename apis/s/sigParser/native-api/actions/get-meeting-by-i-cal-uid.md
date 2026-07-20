# Get Meeting By ICalUID with SigParser

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Meetings/Distinct`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [Get Meeting By ICalUID](https://ipaas.sigparser.com/v1#get-api-meetings-distinct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `icaluid` | query | `string` | yes | Meeting iCal UID to filter by. |
