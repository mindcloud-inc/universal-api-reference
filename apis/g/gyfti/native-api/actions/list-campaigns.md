# List Campaigns with gyfti

Retrieves campaigns from gyfti.

## Endpoint

- **Method:** `GET`
- **Path:** `/obj/Campaign`
- **Base URL:** `https://app.gyfti.fr/api/1.1`
- **Official documentation:** [List Campaigns](https://developer.gyfti.fr/automate-your-gifts/retrieve-your-gyfti-campaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `constraints` | query | `string` | no | Optional URL-safe JSON array of Bubble search constraints, such as [{"key":"Campaign Type","constraint_type":"equals","value":"Trigger"}]. |
