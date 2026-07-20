# List Participations with Reteach

## Endpoint

- **Method:** `GET`
- **Path:** `/participation`
- **Base URL:** `https://api.reteach.io`
- **Official documentation:** [List Participations](https://api.reteach.io/docs/#/Participation/CustomerCourseParticipationController_findMany)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerIdentifier` | query | `string` | no | Filter by the customer id, email, username, or externalId. |
| `courseId` | query | `string` | no | Filter by the id of the course. |
| `customerCertificateId` | query | `string` | no | Filter by the id of the customer certificate. |
| `externalId` | query | `string` | no | Filter participations by externalId. |
| `hasExternalId` | query | `boolean` | no | Filter for participations with or without externalId. |
| `status` | query | `string` | no | Filter by participation status. Multiple values can be comma-separated. Send multiple values as a array separated by `,`. |
| `completedAtSince` | query | `string` | no | Filter for completed participations since a specific date. |
| `hasCertificate` | query | `boolean` | no | Filter for participations with or without certificate. |
| `isExpired` | query | `boolean` | no | Filter for expired or non-expired participations. |
| `isRequired` | query | `boolean` | no | Filter for required or non-required participations. |
