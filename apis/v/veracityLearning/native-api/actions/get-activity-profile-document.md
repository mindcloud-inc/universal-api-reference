# Get Activity Profile Document with Veracity Learning

Retrieves an activity profile document from Veracity Learning.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities/profile`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [Get Activity Profile Document](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | query | `string` | yes | Target activity IRI. |
| `profileId` | query | `string` | yes | Exact activity profile document identifier. |
