# <img src="https://images.mindcloud.co/apps/icons/openfda-icon_1776797355202.png" alt="OpenFDA logo" width="28" height="28"> OpenFDA: Universal API

Public FDA datasets exposed through the openFDA API, including drug, device, food, animal and veterinary, cosmetic, tobacco, transparency, and other FDA records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openFDA/latest
- **Actions:** 57
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://open.fda.gov/
- **Vendor API docs:** https://open.fda.gov/apis/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Count Animal Veterinary Event Records](actions/count-animal-veterinary-event-records.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFDA/latest/actions/count-animal-veterinary-event-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (57)

### Openfda Download Metadata

| Action | Method | Description |
| --- | --- | --- |
| [List OpenFDA Download Metadata](actions/list-openfda-download-metadata.md) | GET | Retrieves download metadata for OpenFDA datasets. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Count Animal Veterinary Event Records](actions/count-animal-veterinary-event-records.md) | GET | Counts animal veterinary event records in OpenFDA. |
| [Count Complete Response Letter Records](actions/count-complete-response-letter-records.md) | GET | Counts complete response letter records in OpenFDA. |
| [Count Cosmetic Event Records](actions/count-cosmetic-event-records.md) | GET | Counts cosmetic event records in OpenFDA. |
| [Count Device Classification Records](actions/count-device-classification-records.md) | GET | Counts device classification records in OpenFDA. |
| [Count Device COVID-19 Serology Records](actions/count-device-covid19-serology-records.md) | GET | Counts device COVID-19 serology records in OpenFDA. |
| [Count Device Enforcement Records](actions/count-device-enforcement-records.md) | GET | Counts device enforcement records in OpenFDA. |
| [Count Device Event Records](actions/count-device-event-records.md) | GET | Counts device event records in OpenFDA. |
| [Count Device PMA Records](actions/count-device-pma-records.md) | GET | Counts device PMA records in OpenFDA. |
| [Count Device Recall Records](actions/count-device-recall-records.md) | GET | Counts device recall records in OpenFDA. |
| [Count Device Registration Listing Records](actions/count-device-registration-listing-records.md) | GET | Counts device registration listing records in OpenFDA. |
| [Count Device UDI Records](actions/count-device-udi-records.md) | GET | Counts device UDI records in OpenFDA. |
| [Count Device 510(k) Records](actions/count-device510k-records.md) | GET | Counts device 510(k) records in OpenFDA. |
| [Count Drug Adverse Event Records](actions/count-drug-adverse-event-records.md) | GET | Counts drug adverse event records in OpenFDA. |
| [Count Drug Enforcement Records](actions/count-drug-enforcement-records.md) | GET | Counts drug enforcement records in OpenFDA. |
| [Count Drug Label Records](actions/count-drug-label-records.md) | GET | Counts drug label records in OpenFDA. |
| [Count Drug NDC Records](actions/count-drug-ndc-records.md) | GET | Counts drug NDC records in OpenFDA. |
| [Count Drug Shortage Records](actions/count-drug-shortage-records.md) | GET | Counts drug shortage records in OpenFDA. |
| [Count Drugs@FDA Records](actions/count-drugs-fda-records.md) | GET | Counts Drugs@FDA records in OpenFDA. |
| [Count Food Enforcement Records](actions/count-food-enforcement-records.md) | GET | Counts food enforcement records in OpenFDA. |
| [Count Food Event Records](actions/count-food-event-records.md) | GET | Counts food event records in OpenFDA. |
| [Count Historical Document Records](actions/count-historical-document-records.md) | GET | Counts historical document records in OpenFDA. |
| [Count NDC SPL Data Element Records](actions/count-ndc-spl-data-element-records.md) | GET | Counts NDC SPL data element records in OpenFDA. |
| [Count Substance Data Records](actions/count-substance-data-records.md) | GET | Counts substance data records in OpenFDA. |
| [Count Tobacco Digital Ads Research Records](actions/count-tobacco-digital-ads-research-records.md) | GET | Counts tobacco digital ads research records in OpenFDA. |
| [Count Tobacco Prevention Ads Research Records](actions/count-tobacco-prevention-ads-research-records.md) | GET | Counts tobacco prevention ads research records in OpenFDA. |
| [Count Tobacco Problem Records](actions/count-tobacco-problem-records.md) | GET | Counts tobacco problem records in OpenFDA. |
| [Count Tobacco Smokefree Research Records](actions/count-tobacco-smokefree-research-records.md) | GET | Counts tobacco smokefree research records in OpenFDA. |
| [Count UNII Records](actions/count-unii-records.md) | GET | Counts UNII records in OpenFDA. |
| [Search Animal Veterinary Event Records](actions/search-animal-veterinary-event-records.md) | GET | Finds animal veterinary event records in OpenFDA. |
| [Search Complete Response Letter Records](actions/search-complete-response-letter-records.md) | GET | Finds complete response letter records in OpenFDA. |
| [Search Cosmetic Event Records](actions/search-cosmetic-event-records.md) | GET | Finds cosmetic event records in OpenFDA. |
| [Search Device Classification Records](actions/search-device-classification-records.md) | GET | Finds device classification records in OpenFDA. |
| [Search Device COVID-19 Serology Records](actions/search-device-covid19-serology-records.md) | GET | Finds device COVID-19 serology records in OpenFDA. |
| [Search Device Enforcement Records](actions/search-device-enforcement-records.md) | GET | Finds device enforcement records in OpenFDA. |
| [Search Device Event Records](actions/search-device-event-records.md) | GET | Finds device event records in OpenFDA. |
| [Search Device PMA Records](actions/search-device-pma-records.md) | GET | Finds device PMA records in OpenFDA. |
| [Search Device Recall Records](actions/search-device-recall-records.md) | GET | Finds device recall records in OpenFDA. |
| [Search Device Registration Listing Records](actions/search-device-registration-listing-records.md) | GET | Finds device registration listing records in OpenFDA. |
| [Search Device UDI Records](actions/search-device-udi-records.md) | GET | Finds device UDI records in OpenFDA. |
| [Search Device 510(k) Records](actions/search-device510k-records.md) | GET | Finds device 510(k) records in OpenFDA. |
| [Search Drug Adverse Event Records](actions/search-drug-adverse-event-records.md) | GET | Finds drug adverse event records in OpenFDA. |
| [Search Drug Enforcement Records](actions/search-drug-enforcement-records.md) | GET | Finds drug enforcement records in OpenFDA. |
| [Search Drug Label Records](actions/search-drug-label-records.md) | GET | Finds drug label records in OpenFDA. |
| [Search Drug NDC Records](actions/search-drug-ndc-records.md) | GET | Finds drug NDC records in OpenFDA. |
| [Search Drug Shortage Records](actions/search-drug-shortage-records.md) | GET | Finds drug shortage records in OpenFDA. |
| [Search Drugs@FDA Records](actions/search-drugs-fda-records.md) | GET | Finds Drugs@FDA records in OpenFDA. |
| [Search Food Enforcement Records](actions/search-food-enforcement-records.md) | GET | Finds food enforcement records in OpenFDA. |
| [Search Food Event Records](actions/search-food-event-records.md) | GET | Finds food event records in OpenFDA. |
| [Search Historical Document Records](actions/search-historical-document-records.md) | GET | Finds historical document records in OpenFDA. |
| [Search NDC SPL Data Element Records](actions/search-ndc-spl-data-element-records.md) | GET | Finds NDC SPL data element records in OpenFDA. |
| [Search Substance Data Records](actions/search-substance-data-records.md) | GET | Finds substance data records in OpenFDA. |
| [Search Tobacco Digital Ads Research Records](actions/search-tobacco-digital-ads-research-records.md) | GET | Finds tobacco digital ads research records in OpenFDA. |
| [Search Tobacco Prevention Ads Research Records](actions/search-tobacco-prevention-ads-research-records.md) | GET | Finds tobacco prevention ads research records in OpenFDA. |
| [Search Tobacco Problem Records](actions/search-tobacco-problem-records.md) | GET | Finds tobacco problem records in OpenFDA. |
| [Search Tobacco Smokefree Research Records](actions/search-tobacco-smokefree-research-records.md) | GET | Finds tobacco smokefree research records in OpenFDA. |
| [Search UNII Records](actions/search-unii-records.md) | GET | Finds UNII records in OpenFDA. |

