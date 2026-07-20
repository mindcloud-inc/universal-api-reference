# Update Robot Cookies with Browse AI

Updates robot cookies in Browse AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/robots/:robotId/cookies`
- **Base URL:** `https://api.browse.ai/v2`
- **Official documentation:** [Update Robot Cookies](https://developers.browse.ai/v2#tag/robots/PATCH/robots/{robotId}/cookies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `robotId` | path | `string` | yes | Unique robot ID  You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. |
| `cookies[]` | body | `array<object>` | yes | Array of cookies to store on the robot. |
| `cookies[]` | body | `array<object>` | yes | Array of cookies to store on the robot. |
