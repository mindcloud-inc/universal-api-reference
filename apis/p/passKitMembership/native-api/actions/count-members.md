# Count Members with PassKit Membership

Retrieves a filtered member count from a PassKit Membership program.

## Endpoint

- **Method:** `POST`
- **Path:** `/members/count/:programId`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Count Members](https://help.passkit.com/en/articles/4133757-membership-protocol-filtering-listing-and-counting-by-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programId` | path | `string` | yes | PassKit program id to count members for. |
