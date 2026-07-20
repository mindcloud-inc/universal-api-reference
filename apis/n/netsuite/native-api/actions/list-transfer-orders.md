# List Transfer Orders with NetSuite - Advanced

## Endpoint

- **Method:** `POST`
- **Path:** `https://{accountId}.restlets.api.netsuite.com/app/site/hosting/restlet.nl`
- **Base URL:** `https://{accountId}.suitetalk.api.netsuite.com`
- **API:** REST
- **Official documentation:** [List Transfer Orders](https://www.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2017_1/script/record/transferorder.html)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns` | body | `object` | no | — |
| `includeAllSublists` | body | `boolean` | no | Format: `toggle`. |
