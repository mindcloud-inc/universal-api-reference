# Delete Activity Profile Document with Veracity Learning

Deletes an activity profile document from Veracity Learning.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/activities/profile`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [Delete Activity Profile Document](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | query | `string` | yes | Target activity IRI. |
| `profileId` | query | `string` | yes | Exact activity profile document identifier. |
