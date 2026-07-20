# List Onboarding Requests with UpGuard

Retrieves onboarding requests from your UpGuard account.

## Endpoint

- **Method:** `GET`
- **Path:** `/onboarding_request/list`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [List Onboarding Requests](https://cyber-risk.upguard.com/api/docs#operation/onboardingRequestsList)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter onboarding requests by status. |
| `archived` | query | `boolean` | no | Filter onboarding requests by archived status. |
| `filter_text` | query | `string` | no | Search text to match vendor name or submitter name. |
