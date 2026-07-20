# Get Analytics DNSSEC with NextDNS

Retrieves DNSSEC validation counts from NextDNS analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles/:profile/analytics/dnssec`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Get Analytics DNSSEC](https://nextdns.io/api#profilesprofileanalyticsdnssec)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. |
| `from` | query | `date` | no | Filter out entities with older date, inclusive. |
| `to` | query | `date` | no | Filter out entities with newer or equal date, exclusive. |
| `limit` | query | `number` | no | Limit the number of results returned. |
| `cursor` | query | `string` | no | Use the pagination cursor returned by the previous response. |
| `device` | query | `string` | no | Only get entities related to a specific device. |
