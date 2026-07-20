# Update Customer with NetSuite - Advanced

## Endpoint

- **Method:** `POST`
- **Path:** `https://{accountId}.restlets.api.netsuite.com/app/site/hosting/restlet.nl`
- **Base URL:** `https://{accountId}.suitetalk.api.netsuite.com`
- **API:** REST
- **Official documentation:** [Update Customer](https://system.netsuite.com/help/helpcenter/en_US/srbrowser/Browser2024_2/script/record/customer.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recordId` | body | `list<number>` | no |
| `columns` | body | `object` | no |
