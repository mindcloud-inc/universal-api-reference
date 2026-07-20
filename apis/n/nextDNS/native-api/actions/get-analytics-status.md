# Get Analytics Status with NextDNS

Retrieves query counts by status from NextDNS analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles/:profile/analytics/status`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Get Analytics Status](https://nextdns.io/api#profilesprofileanalyticsstatus)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
| `from` | query | `date` | no | Filter out entities with older date, inclusive. |
| `to` | query | `date` | no | Filter out entities with newer or equal date, exclusive. |
| `limit` | query | `number` | no | Limit the number of results returned. |
| `cursor` | query | `string` | no | Use the pagination cursor returned by the previous response. |
| `device` | query | `string` | no | Only get entities related to a specific device. |
