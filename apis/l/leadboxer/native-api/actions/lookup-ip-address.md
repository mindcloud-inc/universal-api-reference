# Lookup IP Address with Leadboxer

Finds organization details in Leadboxer by IP address.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/ip-lookup`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Lookup IP Address](https://developers.leadboxer.com/reference/lookupip)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | yes | LeadBoxer account identifier for the tenant whose lookup credits you want to use. |
| `ip` | query | `string` | yes | IP address to enrich, such as 8.8.8.8. |
