# Get Service Site by SMServiceSiteID with Viewpoint Vista

Represents Info, Serviceable Items, Contacts and Notes tabs data found in Viewpoint® Vista™ SM Service Site program.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/sm/2/data/service_sites/cache/id/:SMServiceSiteID`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Get Service Site by SMServiceSiteID](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistasm2datacustomerscachesearchsearch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SMServiceSiteID` | path | `string` | yes | The SMCustomerID portion of the key used to identify the object. |
