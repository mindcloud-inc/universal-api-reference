# Get Customer by SMCo, CustGroup, Customer with Viewpoint Vista

Represents Info, Contacts and Notes tabs data found in Viewpoint® Vista™ SM Customer program.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/sm/2/data/customers/cache/natural/:SMCo/:CustGroup/:Customer`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Get Customer by SMCo, CustGroup, Customer](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistasm2datacustomerscachesearchsearch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SMCo` | path | `string` | yes | The SMCo portion of the key used to identify the object. |
| `CustGroup` | path | `string` | yes | The CustGroup portion of the key used to identify the object. |
| `Customer` | path | `string` | yes | The Customer portion of the key used to identify the object. |
