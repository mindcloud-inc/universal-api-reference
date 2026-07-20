# Lookup Domain with Leadboxer

Finds organization details in Leadboxer by domain name.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/domain-lookup`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Lookup Domain](https://developers.leadboxer.com/reference/lookupdomain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | yes | LeadBoxer account identifier for the tenant whose lookup credits you want to use. |
| `domain` | query | `string` | yes | Company domain to enrich, such as example.com. |
