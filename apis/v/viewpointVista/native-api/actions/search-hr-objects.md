# Search HR Objects with Viewpoint Vista

Search objects found in Viewpoint® Vista™ Human Resources (HR) programs.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Search HR Objects](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedUtcAfter` | body | `date` | no | — |
| `object` | path | `list<string>` | yes | Specify the type of Object from the Human Resources V2 Direct API that you'd like to retrieve. |
| `modifiedUtcBefore` | body | `date` | no | — |
| `filters[]` | body | `array<object>` | no | — |
| `filters` | body | `object` | no | — |
| `filters[].operator` | body | `string` | no | — |
| `filters[].propertyName` | body | `string` | no | — |
| `filters[].value` | body | `string` | no | — |
| `filters[].numberValue` | body | `number` | no | — |
