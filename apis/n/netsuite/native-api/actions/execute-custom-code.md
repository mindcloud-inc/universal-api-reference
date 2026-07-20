# Execute Custom Code with NetSuite - Advanced

Execute custom code using the SuiteScript scripting language

## Endpoint

- **Method:** `POST`
- **Path:** `https://{accountId}.restlets.api.netsuite.com/app/site/hosting/restlet.nl`
- **Base URL:** `https://{accountId}.suitetalk.api.netsuite.com`
- **API:** REST
- **Official documentation:** [Execute Custom Code](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/article_163726005075.html#subsect_164988373340)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eval` | body | `string` | no |
