# Create SSCC Codes with Dachser

Creates SSCC codes for shipments in Dachser.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/ssccs`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Create SSCC Codes](https://api-portal.dachser.com/bi.b2b.portal/api/library/sscc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | body | `number` | no | Number of SSCCs to generate. Maximum 100. |
| `usePrefix` | body | `boolean` | no | Whether to return SSCCs with the 00 prefix. |
