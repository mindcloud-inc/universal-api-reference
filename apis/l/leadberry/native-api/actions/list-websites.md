# List Websites with Leadberry

## Endpoint

- **Method:** `POST`
- **Path:** `/data/getAccounts`
- **Base URL:** `https://app.leadberry.com`
- **Official documentation:** [List Websites](https://www.leadberry.com/zapier)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | body | `string` | no | Filter websites by search text. |
| `accountType` | body | `string` | no | Filter websites by Leadberry account type. |
| `startDate` | body | `date` | no | Filter websites starting from this date. |
| `endDate` | body | `date` | no | Filter websites up to this date. |
