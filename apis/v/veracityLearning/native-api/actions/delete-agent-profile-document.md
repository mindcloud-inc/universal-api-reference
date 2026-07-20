# Delete Agent Profile Document with Veracity Learning

Deletes an agent profile document from Veracity Learning.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/agents/profile`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [Delete Agent Profile Document](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent` | query | `object` | yes | xAPI Agent JSON object identifying the learner or actor. |
| `profileId` | query | `string` | yes | Exact agent profile document identifier. |
