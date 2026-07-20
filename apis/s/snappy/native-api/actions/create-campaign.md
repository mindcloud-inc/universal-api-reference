# Create Campaign with Snappy

Creates a new campaign in Snappy.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Create Campaign](https://docs.snappy.com/reference/createcampaign-1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | body | `string` | yes |
| `companyId` | query | `string` | yes |
| `customization` | body | `object` | yes |
| `name` | body | `string` | yes |
