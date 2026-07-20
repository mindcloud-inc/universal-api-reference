# Enrol Customer with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/enrol/:campaignId`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Enrol Customer](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_enrolMember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Published campaign ID to enrol into. |
| `firstName` | body | `string` | yes | Customer first name. |
| `emailAddress` | body | `string` | yes | Customer email address. |
| `mobileNumber` | body | `string` | yes | Customer mobile number. |
| `dataConsentOptIn` | body | `boolean` | no | Whether the customer opted into data consent. |
| `timeZoneOffset` | body | `string` | no | Optional timezone offset in minutes for expiry-aware campaigns. |
