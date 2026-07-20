# List Client Contacts with Evoliz

Retrieves client contacts from Evoliz.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/contacts-clients`
- **Base URL:** `https://www.evoliz.io`
- **Official documentation:** [List Client Contacts](https://evoliz.io/documentation#tag/Contact%20client/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1contacts-clients/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientid` | query | `number` | no | Optional filter for one client. |
