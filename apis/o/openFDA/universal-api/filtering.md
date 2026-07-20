# OpenFDA Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format OpenFDA expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## OpenFDA actions that support filtering

- [Count Animal Veterinary Event Records](actions/count-animal-veterinary-event-records.md)
- [Count Complete Response Letter Records](actions/count-complete-response-letter-records.md)
- [Count Cosmetic Event Records](actions/count-cosmetic-event-records.md)
- [Count Device Classification Records](actions/count-device-classification-records.md)
- [Count Device COVID-19 Serology Records](actions/count-device-covid19-serology-records.md)
- [Count Device Enforcement Records](actions/count-device-enforcement-records.md)
- [Count Device Event Records](actions/count-device-event-records.md)
- [Count Device PMA Records](actions/count-device-pma-records.md)
- [Count Device Recall Records](actions/count-device-recall-records.md)
- [Count Device Registration Listing Records](actions/count-device-registration-listing-records.md)
- [Count Device UDI Records](actions/count-device-udi-records.md)
- [Count Device 510(k) Records](actions/count-device510k-records.md)
- [Count Drug Adverse Event Records](actions/count-drug-adverse-event-records.md)
- [Count Drug Enforcement Records](actions/count-drug-enforcement-records.md)
- [Count Drug Label Records](actions/count-drug-label-records.md)
- [Count Drug NDC Records](actions/count-drug-ndc-records.md)
- [Count Drug Shortage Records](actions/count-drug-shortage-records.md)
- [Count Drugs@FDA Records](actions/count-drugs-fda-records.md)
- [Count Food Enforcement Records](actions/count-food-enforcement-records.md)
- [Count Food Event Records](actions/count-food-event-records.md)
- [Count Historical Document Records](actions/count-historical-document-records.md)
- [Count NDC SPL Data Element Records](actions/count-ndc-spl-data-element-records.md)
- [Count Substance Data Records](actions/count-substance-data-records.md)
- [Count Tobacco Digital Ads Research Records](actions/count-tobacco-digital-ads-research-records.md)
- [Count Tobacco Prevention Ads Research Records](actions/count-tobacco-prevention-ads-research-records.md)
- [Count Tobacco Problem Records](actions/count-tobacco-problem-records.md)
- [Count Tobacco Smokefree Research Records](actions/count-tobacco-smokefree-research-records.md)
- [Count UNII Records](actions/count-unii-records.md)
- [Search Animal Veterinary Event Records](actions/search-animal-veterinary-event-records.md)
- [Search Complete Response Letter Records](actions/search-complete-response-letter-records.md)
- [Search Cosmetic Event Records](actions/search-cosmetic-event-records.md)
- [Search Device Classification Records](actions/search-device-classification-records.md)
- [Search Device COVID-19 Serology Records](actions/search-device-covid19-serology-records.md)
- [Search Device Enforcement Records](actions/search-device-enforcement-records.md)
- [Search Device Event Records](actions/search-device-event-records.md)
- [Search Device PMA Records](actions/search-device-pma-records.md)
- [Search Device Recall Records](actions/search-device-recall-records.md)
- [Search Device Registration Listing Records](actions/search-device-registration-listing-records.md)
- [Search Device UDI Records](actions/search-device-udi-records.md)
- [Search Device 510(k) Records](actions/search-device510k-records.md)
- [Search Drug Adverse Event Records](actions/search-drug-adverse-event-records.md)
- [Search Drug Enforcement Records](actions/search-drug-enforcement-records.md)
- [Search Drug Label Records](actions/search-drug-label-records.md)
- [Search Drug NDC Records](actions/search-drug-ndc-records.md)
- [Search Drug Shortage Records](actions/search-drug-shortage-records.md)
- [Search Drugs@FDA Records](actions/search-drugs-fda-records.md)
- [Search Food Enforcement Records](actions/search-food-enforcement-records.md)
- [Search Food Event Records](actions/search-food-event-records.md)
- [Search Historical Document Records](actions/search-historical-document-records.md)
- [Search NDC SPL Data Element Records](actions/search-ndc-spl-data-element-records.md)
- [Search Substance Data Records](actions/search-substance-data-records.md)
- [Search Tobacco Digital Ads Research Records](actions/search-tobacco-digital-ads-research-records.md)
- [Search Tobacco Prevention Ads Research Records](actions/search-tobacco-prevention-ads-research-records.md)
- [Search Tobacco Problem Records](actions/search-tobacco-problem-records.md)
- [Search Tobacco Smokefree Research Records](actions/search-tobacco-smokefree-research-records.md)
- [Search UNII Records](actions/search-unii-records.md)
