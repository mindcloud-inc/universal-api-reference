# Get Member By External ID with PassKit Membership

Retrieves a member from PassKit Membership by external ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/members/member/externalId/:programId/:externalId`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Get Member By External ID](https://docs.passkit.io/protocols/member/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | path | `string` | yes | Member external id. |
| `programId` | path | `string` | yes | PassKit membership program id. |
