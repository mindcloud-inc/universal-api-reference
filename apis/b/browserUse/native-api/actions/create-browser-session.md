# Create Browser Session with Browser Use

Creates a browser session in Browser Use.

## Endpoint

- **Method:** `POST`
- **Path:** `/browsers`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [Create Browser Session](https://docs.browser-use.com/cloud/api-v3/browsers/create-browser-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allowResizing` | body | `boolean` | no | Whether to allow browser resizing during the session. |
| `browserScreenHeight` | body | `number` | no | Custom browser screen height in pixels. |
| `browserScreenWidth` | body | `number` | no | Custom browser screen width in pixels. |
| `enableRecording` | body | `boolean` | no | Whether to enable session recording. |
| `profileId` | body | `string` | no | Profile ID to use for the browser session. |
| `proxyCountryCode` | body | `string` | no | Proxy country code. Defaults to us; null disables proxy. |
| `timeout` | body | `number` | no | Session timeout in minutes, 1 to 240. |
