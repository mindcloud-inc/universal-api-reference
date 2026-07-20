# <img src="https://images.mindcloud.co/apps/icons/n-htsavpic_1777575720523.png" alt="NHTSA vPIC logo" width="28" height="28"> NHTSA vPIC: Universal API

Decode VINs and browse NHTSA vehicle makes, models, and manufacturers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nHTSAVPIC/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vpic.nhtsa.dot.gov
- **Vendor API docs:** https://vpic.nhtsa.dot.gov/api/Home/Index

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Manufacturers](actions/list-manufacturers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-manufacturers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Make

| Action | Method | Description |
| --- | --- | --- |
| [List Makes](actions/list-makes.md) | GET | Retrieves vehicle makes from NHTSA vPIC. |
| [List Makes for Manufacturer](actions/list-makes-for-manufacturer.md) | GET | Retrieves makes for a manufacturer from NHTSA vPIC. |
| [List Makes for Manufacturer and Year](actions/list-makes-for-manufacturer-and-year.md) | GET | Retrieves makes for a manufacturer and year from NHTSA vPIC. |
| [List Makes for Vehicle Type](actions/list-makes-for-vehicle-type.md) | GET | Retrieves makes for a vehicle type from NHTSA vPIC. |

### Manufacturer

| Action | Method | Description |
| --- | --- | --- |
| [Get Manufacturer Details](actions/get-manufacturer-details.md) | GET | Retrieves manufacturer details from NHTSA vPIC. |
| [List Manufacturers](actions/list-manufacturers.md) | GET | Retrieves manufacturers from NHTSA vPIC. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [List Models for Make](actions/list-models-for-make.md) | GET | Retrieves models for a make from NHTSA vPIC. |
| [List Models for Make and Year](actions/list-models-for-make-and-year.md) | GET | Retrieves models for a make and year from NHTSA vPIC. |
| [List Models for Make ID](actions/list-models-for-make-id.md) | GET | Retrieves models for a make ID from NHTSA vPIC. |
| [List Models for Make ID and Year](actions/list-models-for-make-id-and-year.md) | GET | Retrieves models for a make ID and year from NHTSA vPIC. |

### Vehicle Type

| Action | Method | Description |
| --- | --- | --- |
| [List Vehicle Types for Make](actions/list-vehicle-types-for-make.md) | GET | Retrieves vehicle types for a make from NHTSA vPIC. |
| [List Vehicle Types for Make ID](actions/list-vehicle-types-for-make-id.md) | GET | Retrieves vehicle types for a make ID from NHTSA vPIC. |

### Vehicle Variable

| Action | Method | Description |
| --- | --- | --- |
| [List Vehicle Variables](actions/list-vehicle-variables.md) | GET | Retrieves vehicle variables from NHTSA vPIC. |

### Vehicle Variable Value

| Action | Method | Description |
| --- | --- | --- |
| [List Vehicle Variable Values](actions/list-vehicle-variable-values.md) | GET | Retrieves vehicle variable values from NHTSA vPIC. |

### Vin Decode Result

| Action | Method | Description |
| --- | --- | --- |
| [Decode VIN](actions/decode-vin.md) | GET | Decodes a VIN with NHTSA vPIC. |
| [Decode VIN Extended](actions/decode-vin-extended.md) | GET | Decodes a VIN with extended data from NHTSA vPIC. |

### Vin Decode Values

| Action | Method | Description |
| --- | --- | --- |
| [Decode VIN Values](actions/decode-vin-values.md) | GET | Retrieves flat decoded VIN values from NHTSA vPIC. |
| [Decode VIN Values Extended](actions/decode-vin-values-extended.md) | GET | Retrieves extended flat decoded VIN values from NHTSA vPIC. |

### Wmi

| Action | Method | Description |
| --- | --- | --- |
| [Decode WMI](actions/decode-wmi.md) | GET | Decodes a WMI with NHTSA vPIC. |
| [List WMIs for Manufacturer](actions/list-wmis-for-manufacturer.md) | GET | Retrieves WMIs for a manufacturer from NHTSA vPIC. |

