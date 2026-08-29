# Get Courses with AXL

## Endpoint

- **Method:** `GET`
- **Path:** `/course`
- **Base URL:** `https://app.axl.tech/api/v1`
- **Official documentation:** [Get Courses](https://app.axl.tech/api/public)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | yes | Fields to return using AXL field-selection syntax, for example {id,name,isPublished} |
| `search` | query | `string` | no | Search phrase for matching courses |
