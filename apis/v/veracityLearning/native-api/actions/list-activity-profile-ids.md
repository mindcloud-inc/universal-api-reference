# List Activity Profile IDs with Veracity Learning

Lists activity profile IDs from Veracity Learning.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities/profile`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [List Activity Profile IDs](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | query | `string` | yes | Target activity IRI. |
| `since` | query | `date` | no | Return activity profile IDs updated after this timestamp. |
