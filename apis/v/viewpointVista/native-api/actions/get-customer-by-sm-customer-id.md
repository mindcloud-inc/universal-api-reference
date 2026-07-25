# Get Customer by SMCustomerID with Viewpoint Vista

Represents Info, Contacts and Notes tabs data found in Viewpoint® Vista™ SM Customer program.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/sm/2/data/customers/cache/id/:SMCustomerID`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Get Customer by SMCustomerID](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistasm2datacustomerscachesearchsearch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SMCustomerID` | path | `string` | yes | The SMCustomerID portion of the key used to identify the object. |
