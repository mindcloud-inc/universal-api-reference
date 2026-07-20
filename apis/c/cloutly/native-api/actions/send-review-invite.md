# Send Review Invite with Cloutly

Creates a customer review invite in Cloutly.

## Endpoint

- **Method:** `POST`
- **Path:** `/send-review-invite`
- **Base URL:** `https://app.cloutly.com/api/v1`
- **API:** rest
- **Official documentation:** [Send Review Invite](https://docs.cloutly.com/reviews-sdk-for-marketplace-websites/rest-api/invite-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `string` | yes | Business to send the review invite from. |
| `firstName` | body | `string` | yes | Customer first name. |
| `lastName` | body | `string` | yes | Customer last name. |
| `email` | body | `string` | yes | Customer email address. |
