# Create File with Sage Intacct

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `newfields[].fieldName` | body | `string` | no |
| `newfields[].internalFields[].fieldValue` | body | `string` | no |
| `object` | body | `string` | yes |
| `fields` | body | `string<object>` | yes |
| `newfields[].fieldValue` | body | `string` | no |
| `newfields[].internalFields[].fieldName` | body | `string` | no |
| `entityID` | body | `string` | no |
| `newfields[].fieldIterator` | body | `string` | no |
| `newfields[].internalFields[]` | body | `array<object>` | no |
