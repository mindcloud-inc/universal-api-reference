# Search Collection Objects with Rijksmuseum

## Endpoint

- **Method:** `GET`
- **Path:** `/search/collection`
- **Base URL:** `https://data.rijksmuseum.nl`
- **Official documentation:** [Search Collection Objects](https://data.rijksmuseum.nl/docs/search)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `string` | no | Search for objects by title, such as Night Watch. |
| `creator` | query | `string` | no | Search for objects by creator name, such as Rembrandt van Rijn. |
| `objectNumber` | query | `string` | no | Search by Rijksmuseum object number. Supports wildcards, such as SK-C-5*. |
| `type` | query | `string` | no | Search by object type, such as painting. |
| `material` | query | `string` | no | Search by material, such as canvas or oil paint. |
| `technique` | query | `string` | no | Search by technique used to create the object. |
| `description` | query | `string` | no | Search keywords present in object descriptions. |
| `imageAvailable` | query | `boolean` | no | Filter objects by whether a digital reproduction is available. |
| `creationDate` | query | `string` | no | Search by year or wildcard period, such as 1642 or 16??. |
| `aboutActor` | query | `string` | no | Search for objects depicting or about a person or group by name. |
| `memberOfSetId` | query | `string` | no | Search for objects that are part of a Rijksmuseum set identifier URL. |
| `pageToken` | query | `string` | no | Token from the previous search response next.id URL for pagination. |
