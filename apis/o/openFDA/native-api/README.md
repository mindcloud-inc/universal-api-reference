# OpenFDA: Native API Reference

A consolidated summary of OpenFDA's API configuration and 57 documented operations, with links to official documentation.

- **Official docs:** https://open.fda.gov/apis/
- **API base URL:** `https://api.fda.gov`

## Authentication

### No Authentication

OpenFDA public dataset endpoints can be called without tenant credentials. Optional API keys only increase rate limits and are not required for this app build.

This API does not require request authentication.

[Official authentication documentation](https://open.fda.gov/apis/authentication/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `User-Agent` | `MindCloud OpenFDA App/1.0` |

Responses from this API use JSON. Response data is read from `results`.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Retry behavior

Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (57 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Animal Veterinary Event Records](actions/count-animal-veterinary-event-records.md) | `GET /animalandveterinary/event.json` | [docs](https://open.fda.gov/apis/animalandveterinary/event/how-to-use-the-endpoint/) |
| [Count Complete Response Letter Records](actions/count-complete-response-letter-records.md) | `GET /transparency/crl.json` | [docs](https://open.fda.gov/apis/transparency/completeresponseletters/how-to-use-the-endpoint/) |
| [Count Cosmetic Event Records](actions/count-cosmetic-event-records.md) | `GET /cosmetic/event.json` | [docs](https://open.fda.gov/apis/cosmetic/event/how-to-use-the-endpoint/) |
| [Count Device Classification Records](actions/count-device-classification-records.md) | `GET /device/classification.json` | [docs](https://open.fda.gov/apis/device/classification/how-to-use-the-endpoint/) |
| [Count Device COVID-19 Serology Records](actions/count-device-covid19-serology-records.md) | `GET /device/covid19serology.json` | [docs](https://open.fda.gov/apis/device/covid19serology/how-to-use-the-endpoint/) |
| [Count Device Enforcement Records](actions/count-device-enforcement-records.md) | `GET /device/enforcement.json` | [docs](https://open.fda.gov/apis/device/enforcement/how-to-use-the-endpoint/) |
| [Count Device Event Records](actions/count-device-event-records.md) | `GET /device/event.json` | [docs](https://open.fda.gov/apis/device/event/how-to-use-the-endpoint/) |
| [Count Device PMA Records](actions/count-device-pma-records.md) | `GET /device/pma.json` | [docs](https://open.fda.gov/apis/device/pma/how-to-use-the-endpoint/) |
| [Count Device Recall Records](actions/count-device-recall-records.md) | `GET /device/recall.json` | [docs](https://open.fda.gov/apis/device/recall/how-to-use-the-endpoint/) |
| [Count Device Registration Listing Records](actions/count-device-registration-listing-records.md) | `GET /device/registrationlisting.json` | [docs](https://open.fda.gov/apis/device/registrationlisting/how-to-use-the-endpoint/) |
| [Count Device UDI Records](actions/count-device-udi-records.md) | `GET /device/udi.json` | [docs](https://open.fda.gov/apis/device/udi/how-to-use-the-endpoint/) |
| [Count Device 510(k) Records](actions/count-device510k-records.md) | `GET /device/510k.json` | [docs](https://open.fda.gov/apis/device/510k/how-to-use-the-endpoint/) |
| [Count Drug Adverse Event Records](actions/count-drug-adverse-event-records.md) | `GET /drug/event.json` | [docs](https://open.fda.gov/apis/drug/event/how-to-use-the-endpoint/) |
| [Count Drug Enforcement Records](actions/count-drug-enforcement-records.md) | `GET /drug/enforcement.json` | [docs](https://open.fda.gov/apis/drug/enforcement/how-to-use-the-endpoint/) |
| [Count Drug Label Records](actions/count-drug-label-records.md) | `GET /drug/label.json` | [docs](https://open.fda.gov/apis/drug/label/how-to-use-the-endpoint/) |
| [Count Drug NDC Records](actions/count-drug-ndc-records.md) | `GET /drug/ndc.json` | [docs](https://open.fda.gov/apis/drug/ndc/how-to-use-the-endpoint/) |
| [Count Drug Shortage Records](actions/count-drug-shortage-records.md) | `GET /drug/shortages.json` | [docs](https://open.fda.gov/apis/drug/drugshortages/how-to-use-the-endpoint/) |
| [Count Drugs@FDA Records](actions/count-drugs-fda-records.md) | `GET /drug/drugsfda.json` | [docs](https://open.fda.gov/apis/drug/drugsfda/how-to-use-the-endpoint/) |
| [Count Food Enforcement Records](actions/count-food-enforcement-records.md) | `GET /food/enforcement.json` | [docs](https://open.fda.gov/apis/food/enforcement/how-to-use-the-endpoint/) |
| [Count Food Event Records](actions/count-food-event-records.md) | `GET /food/event.json` | [docs](https://open.fda.gov/apis/food/event/how-to-use-the-endpoint/) |
| [Count Historical Document Records](actions/count-historical-document-records.md) | `GET /other/historicaldocument.json` | [docs](https://open.fda.gov/apis/other/historicaldocument/how-to-use-the-endpoint/) |
| [Count NDC SPL Data Element Records](actions/count-ndc-spl-data-element-records.md) | `GET /other/nsde.json` | [docs](https://open.fda.gov/apis/other/nsde/how-to-use-the-endpoint/) |
| [Count Substance Data Records](actions/count-substance-data-records.md) | `GET /other/substance.json` | [docs](https://open.fda.gov/apis/other/substance/how-to-use-the-endpoint/) |
| [Count Tobacco Digital Ads Research Records](actions/count-tobacco-digital-ads-research-records.md) | `GET /tobacco/researchdigitalads.json` | [docs](https://open.fda.gov/apis/tobacco/researchdigitalads/how-to-use-the-endpoint/) |
| [Count Tobacco Prevention Ads Research Records](actions/count-tobacco-prevention-ads-research-records.md) | `GET /tobacco/researchpreventionads.json` | [docs](https://open.fda.gov/apis/tobacco/researchpreventionads/how-to-use-the-endpoint/) |
| [Count Tobacco Problem Records](actions/count-tobacco-problem-records.md) | `GET /tobacco/problem.json` | [docs](https://open.fda.gov/apis/tobacco/problem/how-to-use-the-endpoint/) |
| [Count Tobacco Smokefree Research Records](actions/count-tobacco-smokefree-research-records.md) | `GET /tobacco/researchsmokefree.json` | [docs](https://open.fda.gov/apis/tobacco/researchsmokefree/how-to-use-the-endpoint/) |
| [Count UNII Records](actions/count-unii-records.md) | `GET /other/unii.json` | [docs](https://open.fda.gov/apis/other/unii/how-to-use-the-endpoint/) |
| [List OpenFDA Download Metadata](actions/list-openfda-download-metadata.md) | `GET /download.json` | [docs](https://open.fda.gov/apis/download-api-fields/) |
| [Search Animal Veterinary Event Records](actions/search-animal-veterinary-event-records.md) | `GET /animalandveterinary/event.json` | [docs](https://open.fda.gov/apis/animalandveterinary/event/how-to-use-the-endpoint/) |
| [Search Complete Response Letter Records](actions/search-complete-response-letter-records.md) | `GET /transparency/crl.json` | [docs](https://open.fda.gov/apis/transparency/completeresponseletters/how-to-use-the-endpoint/) |
| [Search Cosmetic Event Records](actions/search-cosmetic-event-records.md) | `GET /cosmetic/event.json` | [docs](https://open.fda.gov/apis/cosmetic/event/how-to-use-the-endpoint/) |
| [Search Device Classification Records](actions/search-device-classification-records.md) | `GET /device/classification.json` | [docs](https://open.fda.gov/apis/device/classification/how-to-use-the-endpoint/) |
| [Search Device COVID-19 Serology Records](actions/search-device-covid19-serology-records.md) | `GET /device/covid19serology.json` | [docs](https://open.fda.gov/apis/device/covid19serology/how-to-use-the-endpoint/) |
| [Search Device Enforcement Records](actions/search-device-enforcement-records.md) | `GET /device/enforcement.json` | [docs](https://open.fda.gov/apis/device/enforcement/how-to-use-the-endpoint/) |
| [Search Device Event Records](actions/search-device-event-records.md) | `GET /device/event.json` | [docs](https://open.fda.gov/apis/device/event/how-to-use-the-endpoint/) |
| [Search Device PMA Records](actions/search-device-pma-records.md) | `GET /device/pma.json` | [docs](https://open.fda.gov/apis/device/pma/how-to-use-the-endpoint/) |
| [Search Device Recall Records](actions/search-device-recall-records.md) | `GET /device/recall.json` | [docs](https://open.fda.gov/apis/device/recall/how-to-use-the-endpoint/) |
| [Search Device Registration Listing Records](actions/search-device-registration-listing-records.md) | `GET /device/registrationlisting.json` | [docs](https://open.fda.gov/apis/device/registrationlisting/how-to-use-the-endpoint/) |
| [Search Device UDI Records](actions/search-device-udi-records.md) | `GET /device/udi.json` | [docs](https://open.fda.gov/apis/device/udi/how-to-use-the-endpoint/) |
| [Search Device 510(k) Records](actions/search-device510k-records.md) | `GET /device/510k.json` | [docs](https://open.fda.gov/apis/device/510k/how-to-use-the-endpoint/) |
| [Search Drug Adverse Event Records](actions/search-drug-adverse-event-records.md) | `GET /drug/event.json` | [docs](https://open.fda.gov/apis/drug/event/how-to-use-the-endpoint/) |
| [Search Drug Enforcement Records](actions/search-drug-enforcement-records.md) | `GET /drug/enforcement.json` | [docs](https://open.fda.gov/apis/drug/enforcement/how-to-use-the-endpoint/) |
| [Search Drug Label Records](actions/search-drug-label-records.md) | `GET /drug/label.json` | [docs](https://open.fda.gov/apis/drug/label/how-to-use-the-endpoint/) |
| [Search Drug NDC Records](actions/search-drug-ndc-records.md) | `GET /drug/ndc.json` | [docs](https://open.fda.gov/apis/drug/ndc/how-to-use-the-endpoint/) |
| [Search Drug Shortage Records](actions/search-drug-shortage-records.md) | `GET /drug/shortages.json` | [docs](https://open.fda.gov/apis/drug/drugshortages/how-to-use-the-endpoint/) |
| [Search Drugs@FDA Records](actions/search-drugs-fda-records.md) | `GET /drug/drugsfda.json` | [docs](https://open.fda.gov/apis/drug/drugsfda/how-to-use-the-endpoint/) |
| [Search Food Enforcement Records](actions/search-food-enforcement-records.md) | `GET /food/enforcement.json` | [docs](https://open.fda.gov/apis/food/enforcement/how-to-use-the-endpoint/) |
| [Search Food Event Records](actions/search-food-event-records.md) | `GET /food/event.json` | [docs](https://open.fda.gov/apis/food/event/how-to-use-the-endpoint/) |
| [Search Historical Document Records](actions/search-historical-document-records.md) | `GET /other/historicaldocument.json` | [docs](https://open.fda.gov/apis/other/historicaldocument/how-to-use-the-endpoint/) |
| [Search NDC SPL Data Element Records](actions/search-ndc-spl-data-element-records.md) | `GET /other/nsde.json` | [docs](https://open.fda.gov/apis/other/nsde/how-to-use-the-endpoint/) |
| [Search Substance Data Records](actions/search-substance-data-records.md) | `GET /other/substance.json` | [docs](https://open.fda.gov/apis/other/substance/how-to-use-the-endpoint/) |
| [Search Tobacco Digital Ads Research Records](actions/search-tobacco-digital-ads-research-records.md) | `GET /tobacco/researchdigitalads.json` | [docs](https://open.fda.gov/apis/tobacco/researchdigitalads/how-to-use-the-endpoint/) |
| [Search Tobacco Prevention Ads Research Records](actions/search-tobacco-prevention-ads-research-records.md) | `GET /tobacco/researchpreventionads.json` | [docs](https://open.fda.gov/apis/tobacco/researchpreventionads/how-to-use-the-endpoint/) |
| [Search Tobacco Problem Records](actions/search-tobacco-problem-records.md) | `GET /tobacco/problem.json` | [docs](https://open.fda.gov/apis/tobacco/problem/how-to-use-the-endpoint/) |
| [Search Tobacco Smokefree Research Records](actions/search-tobacco-smokefree-research-records.md) | `GET /tobacco/researchsmokefree.json` | [docs](https://open.fda.gov/apis/tobacco/researchsmokefree/how-to-use-the-endpoint/) |
| [Search UNII Records](actions/search-unii-records.md) | `GET /other/unii.json` | [docs](https://open.fda.gov/apis/other/unii/how-to-use-the-endpoint/) |
