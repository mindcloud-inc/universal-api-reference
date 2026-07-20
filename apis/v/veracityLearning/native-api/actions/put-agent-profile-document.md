# Put Agent Profile Document with Veracity Learning

Updates an agent profile document in Veracity Learning.

## Endpoint

- **Method:** `PUT`
- **Path:** `/agents/profile`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [Put Agent Profile Document](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent` | query | `object` | yes | xAPI Agent JSON object identifying the learner or actor. |
| `profileId` | query | `string` | yes | Exact agent profile document identifier. |
| `document` | body | `object` | yes | JSON document to store for this agent profile. |
