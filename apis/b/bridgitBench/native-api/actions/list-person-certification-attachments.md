# List Person Certification Attachments with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/certifications/:certId/attachments`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Person Certification Attachments](https://developers.gobridgit.com/reference/personcertattachments_query)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID |
| `personId` | path | `number` | yes | The person ID |
| `certId` | path | `number` | yes | The certification ID |
| `state` | query | `list<string>` | no | The state of the attachment for filter Accepted values: `All`, `Completed`, `Failed`, `InProgress`. |
| `creatorId` | query | `number` | no | The ID of attachment creator for filter |
