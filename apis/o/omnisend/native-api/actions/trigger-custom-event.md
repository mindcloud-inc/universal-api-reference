# Trigger Custom Event with Omnisend

Triggers a custom event in Omnisend.

## Endpoint

- **Method:** `POST`
- **Path:** `/v5/events`
- **Base URL:** `https://api.omnisend.com`
- **Official documentation:** [Trigger Custom Event](https://api-docs.omnisend.com/reference/post_events)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact` | body | `object` | yes |
| `contact.address` | body | `string` | no |
| `contact.birthdate` | body | `date` | no |
| `contact.city` | body | `string` | no |
| `contact.country` | body | `string` | no |
| `contact.customProperties` | body | `object` | no |
| `contact.email` | body | `string` | no |
| `contact.firstName` | body | `string` | no |
| `contact.gender` | body | `string` | no |
| `contact.id` | body | `string` | no |
| `contact.lastName` | body | `string` | no |
| `contact.phone` | body | `string` | no |
| `contact.postalCode` | body | `string` | no |
| `contact.state` | body | `string` | no |
| `contact.tags[]` | body | `array<string>` | no |
| `eventID` | body | `string` | no |
| `eventName` | body | `string` | yes |
| `eventVersion` | body | `string` | no |
| `origin` | body | `string` | yes |
| `properties` | body | `object` | no |
