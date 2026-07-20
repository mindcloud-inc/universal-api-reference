# Update Learner with Qualiobee

Updates an existing learner in Qualiobee.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:organizationUuid/learner/:learnerUuid`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Update Learner](https://app.qualiobee.fr/api/doc/#/Learner/PublicLearnerController_updateOne)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes |
| `learnerUuid` | path | `string` | yes |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `email` | body | `string` | no |
| `type` | body | `string` | no |
| `jobStatus` | body | `string` | no |
| `birthDate` | body | `string` | no |
| `birthCity` | body | `string` | no |
| `birthDepartment` | body | `string` | no |
| `needsAdaptation` | body | `boolean` | no |
| `phoneNumber` | body | `string` | no |
| `note` | body | `string` | no |
| `location.addressLine1` | body | `string` | no |
| `location.addressLine2` | body | `string` | no |
| `location.postCode` | body | `string` | no |
| `location.city` | body | `string` | no |
| `location.country` | body | `string` | no |
