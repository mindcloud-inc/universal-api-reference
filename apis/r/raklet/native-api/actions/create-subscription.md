# Create Subscription with Raklet

## Endpoint

- **Method:** `POST`
- **Path:** `/organisations/:organisationId/subscriptions`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Create Subscription](https://api.raklet.com/swagger/ui/index#/Subscription/Subscription_AddSubscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationMembershipId` | body | `string` | yes | Contact membership identifier in Raklet. |
| `customMemberTypeId` | body | `string` | yes | Subscription plan/type identifier from Raklet's subscription payload schema. |
| `startDate` | body | `string` | yes | Subscription start date in ISO 8601 format. |
