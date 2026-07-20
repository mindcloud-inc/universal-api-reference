# Delete All State Documents with Veracity Learning

Deletes all state documents from Veracity Learning.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/activities/state`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [Delete All State Documents](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | query | `string` | yes | Target activity IRI. |
| `agent` | query | `object` | yes | xAPI Agent JSON object identifying the learner or actor. |
| `registration` | query | `string` | no | Optional registration UUID. |
