# Get State Document with Veracity Learning

Retrieves a state document from Veracity Learning.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities/state`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [Get State Document](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | query | `string` | yes | Activity id associated with this state document |
| `agent` | query | `object` | yes | Agent object associated with this state document |
| `registration` | query | `string` | no | Registration id associated with this state document |
| `stateId` | query | `string` | yes | State id to load |
