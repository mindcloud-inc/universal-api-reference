# Get Learner with Qualiobee

Retrieves a learner from Qualiobee.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organizationUuid/learner/:learnerUuid`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Get Learner](https://app.qualiobee.fr/api/doc/#/Learner/PublicLearnerController_getOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | — |
| `learnerUuid` | path | `string` | yes | — |
| `withDeleted` | query | `boolean` | no | — |
| `relations` | query | `list<string>` | no | Send multiple values as a array. |
