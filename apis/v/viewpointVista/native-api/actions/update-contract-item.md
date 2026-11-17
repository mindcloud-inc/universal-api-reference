# Update Contract Item with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/jc/2/data/contracts/actions/chg_line`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Update Contract Item](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistajc2datacontractsactionschg_line)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `__key` | body | `object` | yes | Object { "JCCo": number, "Contract": string (≤ 10), "Item": string (≤ 16) }, or { "KeyID": number } of the contract item. |
| `Department` | body | `string` | no | Key to jc/departments(JCCo, Department). Optional. If omitted, existing value in Vista will remain unchanged. Maximum length: 10. |
| `Description` | body | `string` | no | Optional. If omitted, existing value in Vista will remain unchanged. Maximum length: 60. |
