# Removes A Strategy Attached To A Milestone with Unleash

Removes a strategy attached to a milestone from Unleash.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/admin/release-plan-templates/{templateId}/milestones/{milestoneId}/strategies/{strategyId}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Removes A Strategy Attached To A Milestone](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | Required path parameter. |
| `milestoneId` | path | `string` | yes | Required path parameter. |
| `strategyId` | path | `string` | yes | Required path parameter. |
