# Check Keyword Availability with GatewayAPI SMS

Checks whether a keyword is available in GatewayAPI SMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/vas/check`
- **Base URL:** `https://gatewayapi.com`
- **Official documentation:** [Check Keyword Availability](https://gatewayapi.com/docs/apis/keywords/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shortcode` | body | `number` | yes | Shortcode to check the keyword against. |
| `keyword` | body | `string` | yes | Keyword to search for. |
