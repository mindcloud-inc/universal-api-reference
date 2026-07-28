# List Potential Projects with Viewpoint Vista

Represents Potential Project data in Viewpoint® Vista™.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [List Potential Projects](https://direct-api.xchange.trimble.com/reference/get-directsubscriberssubscriber_codevistasm2datacustomerscache)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedUTCSince` | query | `string` | no | Specify a datetime against which to filter the results.  When specified the result will be ordered oldest __modifiedUTC to newest.  Example `2019-12-11T20:16:58.3419275Z`.  ( Optional ) If unspecified, all cached objects will be returned. |
