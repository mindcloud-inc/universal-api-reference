# Acknowledge Alerts with LogMeIn

Updates alerts by acknowledging them in LogMeIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/goto-resolve-alerts/v1/acknowledge`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Acknowledge Alerts](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `acknowledgeData[]` | body | `array<object>` | yes | Array of alert/device pairs to acknowledge. GoTo documents a maximum of 100 items. |
