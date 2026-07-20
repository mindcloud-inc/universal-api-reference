# Update Subscription with Raklet

## Endpoint

- **Method:** `PUT`
- **Path:** `/organisations/:organisationId/subscriptions/:subscriptionId`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Update Subscription](https://api.raklet.com/swagger/ui/index#/Subscription/Subscription_UpdateSubscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `string` | yes | Raklet subscription identifier. |
| `organisationMembershipId` | body | `string` | yes | Contact membership identifier in Raklet. |
| `customMemberTypeId` | body | `string` | yes | Subscription plan/type identifier from Raklet's subscription payload schema. |
| `startDate` | body | `string` | yes | Subscription start date in ISO 8601 format. |
