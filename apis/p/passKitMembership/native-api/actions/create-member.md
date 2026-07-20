# Create Member with PassKit Membership

Creates a member in PassKit Membership.

## Endpoint

- **Method:** `POST`
- **Path:** `/members/member`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Create Member](https://docs.passkit.io/protocols/member/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | body | `string` | yes | External member identifier used to de-duplicate enrolments. |
| `person.displayName` | body | `string` | yes | Display name for the enrolled member. |
| `programId` | body | `string` | yes | PassKit membership program identifier. |
| `tierId` | body | `string` | yes | PassKit membership tier identifier. |
