# List GL Objects with Viewpoint Vista

Represents data found in Viewpoint® Vista™ GL programs.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [List GL Objects](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedUTCSince` | query | `string` | no | Specify a datetime against which to filter the results.  When specified the result will be ordered oldest __modifiedUTC to newest.  Example `2019-12-11T20:16:58.3419275Z`.  ( Optional ) If unspecified, all cached objects will be returned. |
| `object` | path | `list<string>` | yes | Specify the type of Object from the Equipment Management V2 Direct API that you'd like to retrieve. |
