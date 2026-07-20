# Get Subscription by Email with Beehiiv

Retrieves a subscription from Beehiiv by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/subscriptions/by_email/:email`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Get Subscription by Email](https://developers.beehiiv.com/api-reference/subscriptions/get-by-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `email` | path | `string` | yes | Email address (URL-encoded in path). |
| `expand` | query | `string` | no | Optional list of expandable subscription objects. |
