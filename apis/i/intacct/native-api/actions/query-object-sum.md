# Query Object Sum with Sage Intacct

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[].filterfield` | body | `string` | no | — |
| `object` | body | `string` | no | — |
| `options[].caseinsensitive` | body | `boolean` | no | — |
| `fields[]` | body | `array<string>` | yes | — |
| `filter[].filtertype` | body | `list<string>` | no | — |
| `options[].showprivate` | body | `boolean` | no | In a multi-entity company, set the `showprivate` element to `true` to query data in private entities. |
| `filter[]` | body | `array<object>` | no | — |
| `filter[].filtervalue` | body | `string` | no | — |
| `docparid` | body | `string` | no | — |
| `entityID` | body | `string` | no | — |
| `options[]` | body | `array` | no | — |
| `orderBy` | body | `string` | no | — |
| `sumField` | body | `string` | no | Return the sum of the fields. The fields in the select element are used to group the results. |
