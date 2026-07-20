# Get Logs with NextDNS

Retrieves DNS logs from a NextDNS profile.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles/:profile/logs`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Get Logs](https://nextdns.io/api#logs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
| `from` | query | `date` | no | Filter out logs with older date, inclusive. |
| `to` | query | `date` | no | Filter out logs with newer or equal date, exclusive. |
| `sort` | query | `string` | no | Sort logs from oldest to newest or newest to oldest. |
| `limit` | query | `number` | no | Limit the number of results returned. |
| `cursor` | query | `string` | no | Use the pagination cursor returned by the previous response. |
| `device` | query | `string` | no | Only get logs made for a specific device. |
| `status` | query | `string` | no | Filter logs by status. |
| `search` | query | `string` | no | Only return logs matching the search query. |
| `raw` | query | `boolean` | no | When true, return all DNS queries instead of the default filtered view. |
