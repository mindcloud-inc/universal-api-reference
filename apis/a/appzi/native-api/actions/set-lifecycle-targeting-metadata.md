# Set Lifecycle Targeting Metadata with Appzi

Generates Appzi lifecycle targeting metadata settings.

## Endpoint

- **Method:** `GET`
- **Path:** `https://docs.appzi.io/integration/add-data/`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Set Lifecycle Targeting Metadata](https://docs.appzi.io/integration/add-data/#lifecycle-targeting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | query | `string` | yes | Stable user identifier inserted into the generated lifecycle-targeting snippet. |
| `userCreationDate` | query | `string` | yes | ISO 8601 account creation date inserted into the generated lifecycle-targeting snippet. |
