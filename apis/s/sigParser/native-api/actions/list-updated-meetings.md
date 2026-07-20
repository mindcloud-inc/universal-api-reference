# List Updated Meetings with SigParser

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Meetings/Distinct`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [List Updated Meetings](https://ipaas.sigparser.com/v1#get-api-meetings-distinct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastmodified_after` | query | `number` | yes | Return meetings updated after this timestamp key. |
