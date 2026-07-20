# <img src="https://images.mindcloud.co/apps/icons/smarty-streets_1778092360121.png" alt="Smarty-streets logo" width="28" height="28"> Smarty-streets: Universal API

Verify, standardize, enrich, and geocode addresses with Smarty

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smartyStreets/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smarty.com
- **Vendor API docs:** https://www.smarty.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate US Street Address](actions/validate-us-street-address.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-street-address?connectionId=$CONNECTION_ID&street=1%20Santa%20Claus%20Ln&city=North%20Pole&state=AK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Bulk ZIP Code Lookups](actions/bulk-zip-code-lookups.md) | GET | Retrieves ZIP Code lookup details from Smarty-streets in bulk. |
| [Extract US Addresses Aggressively](actions/extract-us-addresses-aggressively.md) | GET | Extracts US addresses from text in Smarty-streets using aggressive matching. |
| [Extract US Addresses From Text](actions/extract-us-addresses-from-text.md) | GET | Extracts US addresses from text in Smarty-streets. |
| [Get Property Data By SmartyKey](actions/get-property-data-by-smarty-key.md) | GET | Retrieves property data from Smarty-streets by SmartyKey. |
| [Lookup International Postal Code](actions/lookup-international-postal-code.md) | GET | Retrieves international postal code details from Smarty-streets by postal code. |
| [Lookup ZIP Code Details](actions/lookup-zip-code-details.md) | GET | Retrieves ZIP Code details from Smarty-streets. |
| [Lookup ZIP Codes By City State](actions/lookup-zip-codes-by-city-state.md) | GET | Finds ZIP Codes in Smarty-streets by city and state. |
| [Reverse Geocode US Coordinates](actions/reverse-geocode-us-coordinates.md) | GET | Finds nearby US addresses in Smarty-streets by latitude and longitude. |
| [Reverse Geocode US Coordinates Including Non Postal Sources](actions/reverse-geocode-us-coordinates-including-non-postal-sources.md) | GET | Finds nearby US addresses in Smarty-streets by coordinates, including non-postal sources. |
| [Suggest International Addresses](actions/suggest-international-addresses.md) | GET | Finds international address suggestions in Smarty-streets by search text. |
| [Suggest US Addresses](actions/suggest-us-addresses.md) | GET | Finds US address suggestions in Smarty-streets by search text. |
| [Validate City State ZIP Combination](actions/validate-city-state-zip-combination.md) | GET | Retrieves validation details for a city, state, and ZIP combination in Smarty-streets. |
| [Validate US Address And Return Invalid Detail](actions/validate-us-address-and-return-invalid-detail.md) | GET | Retrieves US address validation details from Smarty-streets, including invalid matches. |
| [Validate US Address With Component Analysis](actions/validate-us-address-with-component-analysis.md) | GET | Retrieves US address validation details from Smarty-streets with component analysis. |
| [Validate US Address With Enhanced Matching](actions/validate-us-address-with-enhanced-matching.md) | GET | Retrieves US address validation details from Smarty-streets using enhanced matching. |
| [Validate US Address With IANA Timezone](actions/validate-us-address-with-iana-timezone.md) | GET | Retrieves US address validation details from Smarty-streets with IANA timezone data. |
| [Validate US Address With Project USA Format](actions/validate-us-address-with-project-usa-format.md) | GET | Retrieves a validated US address from Smarty-streets in Project USA format. |
| [Validate US Addresses In Bulk](actions/validate-us-addresses-in-bulk.md) | GET | Retrieves validated US addresses from Smarty-streets in bulk. |
| [Validate US Freeform Address](actions/validate-us-freeform-address.md) | GET | Retrieves a validated US freeform address from Smarty-streets. |
| [Validate US Street Address](actions/validate-us-street-address.md) | GET | Retrieves validated US street addresses from Smarty-streets. |
| [Verify International Address](actions/verify-international-address.md) | GET | Retrieves international address verification details from Smarty-streets. |

