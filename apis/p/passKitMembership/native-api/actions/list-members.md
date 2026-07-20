# List Members with PassKit Membership

Retrieves members from a PassKit Membership program.

## Endpoint

- **Method:** `POST`
- **Path:** `/members/member/list/:programId`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [List Members](https://help.passkit.com/en/articles/4133757-membership-protocol-filtering-listing-and-counting-by-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programId` | path | `string` | yes | PassKit Program ID from the target membership program settings page. |
