# Reply to Customer with GatherUp

Creates a reply to a customer in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer/reply`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Reply to Customer](https://app.gatherup.com/api/doc/customer/reply)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | body | `number` | yes | Customer id. |
| `content` | body | `string` | yes | The content of the comment. |
| `title` | body | `string` | no | Your title. |
| `visibility` | body | `number` | no | The visibility the response. Is response public? (1 - yes, 0 - no) |
| `respondAsBusinessOwner` | body | `number` | no | Respond as business owner (otherwise response will be from logged in user, 1 - yes, 0 - no) |
