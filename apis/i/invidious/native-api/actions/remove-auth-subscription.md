# Remove Auth Subscription with Invidious

## Endpoint

- **Method:** `DELETE`
- **Path:** `/auth/subscriptions/:ucid`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Remove Auth Subscription](https://docs.invidious.io/api/authenticated-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ucid` | path | `string` | yes | Channel UCID to unsubscribe from. |
