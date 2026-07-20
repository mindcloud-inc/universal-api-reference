# Upsert Customer Bill-To with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/CustomerBillto`
- **Base URL:** `{url}:8482/`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AltAddr1` | body | `string` | no | — |
| `AltAddr2` | body | `string` | no | — |
| `AltCity` | body | `string` | no | — |
| `AltContact` | body | `string` | no | Bill-to Contact |
| `AltCountry` | body | `string` | no | — |
| `AltEmail` | body | `string` | no | — |
| `AltFax` | body | `string` | no | — |
| `AltName` | body | `string` | no | Bill-to name Required if creating a new Bill-to code. |
| `AltPhone` | body | `string` | no | — |
| `AltState` | body | `string` | no | — |
| `AltZip` | body | `string` | no | — |
| `Billto_Code` | body | `string` | no | — |
| `Customer_Code` | body | `string` | no | — |
| `Remark` | body | `string` | no | — |
| `Status` | body | `string` | no | — |
| `Company_Code` | body | `string` | no | — |
