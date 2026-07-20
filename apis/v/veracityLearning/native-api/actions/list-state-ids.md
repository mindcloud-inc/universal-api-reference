# List State IDs with Veracity Learning

Lists state document IDs from Veracity Learning.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities/state`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [List State IDs](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | query | `string` | yes | Activity id associated with these state documents |
| `agent` | query | `object` | yes | Agent object associated with these state documents |
| `registration` | query | `string` | no | Registration id associated with these state documents |
| `since` | query | `date` | no | Only return state ids updated since this timestamp |
