# Create Item with Sage Intacct

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
| `object` | body | `string` | yes |
| `fieldsjson[]` | body | `array<object>` | yes |
