# List Service Groups with eTermin

Retrieves service groups from eTermin.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/servicegroup`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [List Service Groups](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Servicegroup/get_api_servicegroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `servicegroupid` | query | `number` | no | ID of the servicegroup that you want information on |
| `languageid` | query | `string` | no | Language code if you only want the information for a specific language e.g. DE, EN, etc. |
