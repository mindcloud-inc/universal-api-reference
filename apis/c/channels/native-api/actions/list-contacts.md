# List Contacts with Channels

Retrieves contacts from Channels.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/contacts`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [List Contacts](https://developers.channels.app/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modificationDateFrom` | query | `string` | no | Optional lower bound for contact last modification date. |
| `orderModificationDate` | query | `string` | no | Optional sort direction for contact last modification date; docs allow asc or desc. |
| `msisdn` | query | `string` | no | Optional filter for contacts whose MSISDN contains the provided sequence. |
