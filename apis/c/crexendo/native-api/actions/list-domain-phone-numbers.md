# List Domain Phone Numbers with Crexendo

Retrieves phone numbers for a domain in Crexendo.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/:domain/phonenumbers`
- **Base URL:** `https://ns-api.com/ns-api/v2`
- **Official documentation:** [List Domain Phone Numbers](https://docs.ns-api.com/reference/getdomainphonenumbers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain identifier, for example apps.mindcloud.co. |
