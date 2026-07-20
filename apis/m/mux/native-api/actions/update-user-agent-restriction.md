# Update User Agent Restriction with Mux

## Endpoint

- **Method:** `PUT`
- **Path:** `/video/v1/playback-restrictions/{PLAYBACK_RESTRICTION_ID}/user_agent`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Update User Agent Restriction](https://www.mux.com/docs/api-reference/video/playback-restrictions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allow_high_risk_user_agent` | body | `boolean` | yes | Whether high-risk user agents are allowed. |
| `allow_no_user_agent` | body | `boolean` | yes | Whether requests without a user agent are allowed. |
| `PLAYBACK_RESTRICTION_ID` | path | `string` | yes | The playback restriction ID. |
