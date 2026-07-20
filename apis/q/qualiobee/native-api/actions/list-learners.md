# List Learners with Qualiobee

Retrieves learners from Qualiobee.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organizationUuid/learner`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [List Learners](https://app.qualiobee.fr/api/doc/#/Learner/PublicLearnerController_getMany)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | — |
| `withDeleted` | query | `boolean` | no | — |
| `relations` | query | `list<string>` | no | Send multiple values as a array. |
| `uuid` | query | `string` | no | — |
| `firstName` | query | `string` | no | — |
| `externalId` | query | `string` | no | — |
| `lastName` | query | `string` | no | — |
| `email` | query | `string` | no | — |
| `type` | query | `string` | no | — |
