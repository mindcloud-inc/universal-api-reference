# Delete State Document with Veracity Learning

Deletes a state document from Veracity Learning.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/activities/state`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [Delete State Document](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | query | `string` | yes | Target activity IRI. |
| `agent` | query | `object` | yes | xAPI Agent JSON object identifying the learner or actor. |
| `registration` | query | `string` | no | Optional registration UUID. |
| `stateId` | query | `string` | yes | Exact state document identifier. |
