# Validate a phone number with Routee

Validates a phone number in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/numbervalidator`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Validate a phone number](https://docs.routee.net/reference/validate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `getPorted` | body | `boolean` | no | Indicates if the number validator result will concern the number's ported network (only if the number is ported). Pricing differs if you select this option. Visit [here](https://dev.routee.net/#/management/financial/pricing) for pricing information. Default value: false |
| `to` | body | `string` | yes | The number that the number validator service will use. Format with a '+' and country code (E.164 format). |
| `host` | body | `string` | no | The host name or the IP address. This field is used in order to get information about the country of an IP or a domain name. |
