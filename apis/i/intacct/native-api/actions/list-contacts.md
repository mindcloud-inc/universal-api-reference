# List Contacts with Sage Intacct

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`
- **Official documentation:** [List Contacts](https://developer.intacct.com/api/project-resource-mgmt/projects/#query-and-list-projects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filter[].filterfield` | body | `string` | no |
| `options[].caseinsensitive` | body | `boolean` | no |
| `filter[].filtertype` | body | `list<string>` | no |
| `filter[]` | body | `array<object>` | no |
| `filter[].filtervalue` | body | `string` | no |
| `docparid` | body | `string` | no |
| `entityID` | body | `string` | no |
| `options[]` | body | `array` | no |
