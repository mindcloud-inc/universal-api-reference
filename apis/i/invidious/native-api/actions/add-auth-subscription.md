# Add Auth Subscription with Invidious

## Endpoint

- **Method:** `POST`
- **Path:** `/auth/subscriptions/:ucid`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Add Auth Subscription](https://docs.invidious.io/api/authenticated-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ucid` | path | `string` | yes | Channel UCID to subscribe to. |
