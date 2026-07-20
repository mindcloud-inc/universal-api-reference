# List Tiers with PassKit Membership

Retrieves membership tiers from a PassKit Membership program.

## Endpoint

- **Method:** `POST`
- **Path:** `/members/tiers/list`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [List Tiers](https://help.passkit.com/en/articles/4133757-membership-protocol-filtering-listing-and-counting-by-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programId` | path | `string` | yes | PassKit Program ID used to filter tiers for a membership program. |
