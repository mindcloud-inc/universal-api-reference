# Create Sales Order with NetSuite - Advanced

## Endpoint

- **Method:** `POST`
- **Path:** `https://{accountId}.restlets.api.netsuite.com/app/site/hosting/restlet.nl`
- **Base URL:** `https://{accountId}.suitetalk.api.netsuite.com`
- **API:** REST

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns` | body | `object` | no | — |
| `ignoreMandatoryFields` | body | `boolean` | no | Format: `toggle`. |
