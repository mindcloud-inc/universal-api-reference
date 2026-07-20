# List Branches with TalentLMS

Retrieves branches from a TalentLMS domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/branches`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [List Branches](https://documenter.getpostman.com/view/31867199/2sAY548Kou#list-all-branches)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page[number]` | query | `number` | no | Page number for paginated results. |
| `page[size]` | query | `number` | no | Number of records per page (max 100). |
