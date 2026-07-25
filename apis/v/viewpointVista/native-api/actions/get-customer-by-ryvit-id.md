# Get Customer by RyvitId with Viewpoint Vista

Represents Info, Contacts and Notes tabs data found in Viewpoint® Vista™ SM Customer program.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/sm/2/data/customers/cache/__ryvitId/:ryvitId_value`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Get Customer by RyvitId](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache__ryvitidryvitid_value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ryvitId_value` | path | `string` | yes | The code of the data object you want to get. |
