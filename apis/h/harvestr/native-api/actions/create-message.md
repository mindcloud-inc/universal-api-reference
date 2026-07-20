# Create Message with Harvestr.io

## Endpoint

- **Method:** `POST`
- **Path:** `/message`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [Create Message](https://developers.harvestr.io/api/create-a-message/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `integrationId` | body | `string` | no | Integration ID |
| `integrationUrl` | body | `string` | no | Integration URL |
| `channel` | body | `string` | no | Message channel |
| `title` | body | `string` | yes | Message title |
| `content` | body | `string` | yes | Message content |
| `labels[]` | body | `array<string>` | no | Message labels |
| `requester` | body | `object` | yes | Requester to be upserted |
| `requester.type` | body | `string` | yes | Customer type (USER or COMPANY) |
| `requester.externalUid` | body | `string` | yes | External unique identifier for the customer |
| `requester.email` | body | `string` | yes | Email identifier (only for type: USER) |
| `requester.name` | body | `string` | yes | Customer name (always required) |
| `submitter` | body | `object` | no | Submitter to be upserted (optional) |
| `submitter.externalUid` | body | `string` | no | External unique identifier for the company |
| `submitter.email` | body | `string` | no | Company email |
| `submitter.name` | body | `string` | no | Company name (always required) |
