# Create Learner with Qualiobee

Creates a new learner in Qualiobee.

## Endpoint

- **Method:** `POST`
- **Path:** `/:organizationUuid/learner`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Create Learner](https://app.qualiobee.fr/api/doc/#/Learner/PublicLearnerController_createOne)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes |
| `firstName` | body | `string` | yes |
| `lastName` | body | `string` | yes |
| `email` | body | `string` | yes |
| `type` | body | `string` | yes |
| `customerUuid` | body | `string` | yes |
| `externalId` | body | `string` | no |
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
