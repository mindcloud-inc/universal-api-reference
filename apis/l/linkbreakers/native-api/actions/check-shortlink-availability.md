# Check Shortlink Availability with Linkbreakers

Checks whether a shortlink is available in Linkbreakers.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/links/shortlink-availability`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Check Shortlink Availability](https://linkbreakers.com/help/api/links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shortlink` | query | `string` | no | The shortlink slug to check. |
| `customDomainId` | query | `string` | no | The custom domain ID to check against. |
