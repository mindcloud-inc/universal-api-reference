# Create Opportunity with Autotask

## Endpoint

- **Method:** `POST`
- **Path:** `/Opportunities`
- **Base URL:** `https://webservices14.autotask.net/ATServicesRest/v1.0`
- **Official documentation:** [Create Opportunity](https://www.autotask.net/help/developerhelp/Content/APIs/REST/Entities/OpportunitiesEntity.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyID` | body | `number` | yes | The Autotask company for this opportunity. If Contact ID is provided, the contact must be active and belong to this company or its parent. |
| `title` | body | `string` | yes | The opportunity title. Maximum length: 128. |
| `ownerResourceID` | body | `number` | yes | An active standard Autotask resource with CRM access who owns the opportunity. |
| `amount` | body | `number` | yes | The opportunity total amount. When revenue-period fields are supplied, Autotask recalculates this value. |
| `cost` | body | `number` | yes | The opportunity total cost. When cost-period fields are supplied, Autotask recalculates this value. |
| `probability` | body | `number` | yes | The close probability as a number from 0 through 100. |
| `projectedCloseDate` | body | `date` | yes | The projected close date in YYYY-MM-DD format. It cannot be earlier than the opportunity create date. |
| `stage` | body | `number` | yes | The Autotask opportunity stage value. |
| `status` | body | `number` | yes | The Autotask opportunity status value. |
| `useQuoteTotals` | body | `boolean` | yes | Use quote totals for this opportunity. Set true only when an Autotask quote references the opportunity. |
| `contactID` | body | `number` | no | An active contact associated with Company ID or that company's parent. |
| `opportunityCategoryID` | body | `number` | no | The opportunity category. Autotask applies the selected category's defaults when the opportunity is created. |
| `organizationalLevelAssociationID` | body | `number` | no | The Autotask organizational level association for the opportunity. |
| `productID` | body | `number` | no | The Autotask product associated with the opportunity. |
| `primaryCompetitor` | body | `number` | no | The Autotask primary competitor value. |
| `leadSource` | body | `number` | no | The Autotask lead source value. |
| `rating` | body | `number` | no | The Autotask opportunity rating value. |
| `nextStep` | body | `string` | no | The next planned step for the opportunity. Maximum length: 500. |
| `description` | body | `string` | no | A description of the opportunity. Maximum length: 8000. |
| `barriers` | body | `string` | no | Barriers that may prevent the opportunity from closing. Maximum length: 500. |
| `helpNeeded` | body | `string` | no | Help needed to advance the opportunity. Maximum length: 500. |
| `market` | body | `string` | no | The market associated with the opportunity. Maximum length: 500. |
| `promotionName` | body | `string` | no | The promotion associated with the opportunity. Maximum length: 50. |
| `lossReason` | body | `number` | no | The Autotask loss reason value. |
| `lossReasonDetail` | body | `string` | no | Additional detail explaining why the opportunity was lost. Maximum length: 500. |
| `lostDate` | body | `date` | no | The lost date in YYYY-MM-DD format. Supply it when the opportunity status is Lost. |
| `winReason` | body | `number` | no | The Autotask win reason value. |
| `winReasonDetail` | body | `string` | no | Additional detail explaining why the opportunity was won. Maximum length: 500. |
| `closedDate` | body | `date` | no | The closed date in YYYY-MM-DD format. |
| `promisedFulfillmentDate` | body | `date` | no | The promised fulfillment date in YYYY-MM-DD format. |
| `throughDate` | body | `date` | no | The revenue through date in YYYY-MM-DD format. |
| `revenueSpreadUnit` | body | `string` | no | The Autotask revenue spread unit. When both spread fields are omitted, Autotask uses its all-at-once behavior. Maximum length: 6. |
| `revenueSpread` | body | `number` | no | The revenue spread quantity. Autotask discards it when Revenue Spread Unit is omitted. |
| `totalAmountMonths` | body | `number` | no | The total number of months included in the opportunity amount. |
| `onetimeCost` | body | `number` | no | One-time cost. Billing-period cost inputs cause Autotask to recalculate total Cost. |
| `onetimeRevenue` | body | `number` | no | One-time revenue. Billing-period revenue inputs cause Autotask to recalculate total Amount. |
| `monthlyCost` | body | `number` | no | Monthly cost. Billing-period cost inputs cause Autotask to recalculate total Cost. |
| `monthlyRevenue` | body | `number` | no | Monthly revenue. Billing-period revenue inputs cause Autotask to recalculate total Amount. |
| `quarterlyCost` | body | `number` | no | Quarterly cost. Billing-period cost inputs cause Autotask to recalculate total Cost. |
| `quarterlyRevenue` | body | `number` | no | Quarterly revenue. Billing-period revenue inputs cause Autotask to recalculate total Amount. |
| `semiannualCost` | body | `number` | no | Semiannual cost. Billing-period cost inputs cause Autotask to recalculate total Cost. |
| `semiannualRevenue` | body | `number` | no | Semiannual revenue. Billing-period revenue inputs cause Autotask to recalculate total Amount. |
| `yearlyCost` | body | `number` | no | Yearly cost. Billing-period cost inputs cause Autotask to recalculate total Cost. |
| `yearlyRevenue` | body | `number` | no | Yearly revenue. Billing-period revenue inputs cause Autotask to recalculate total Amount. |
| `advancedField1` | body | `number` | no | Autotask opportunity advanced field 1. |
| `advancedField2` | body | `number` | no | Autotask opportunity advanced field 2. |
| `advancedField3` | body | `number` | no | Autotask opportunity advanced field 3. |
| `advancedField4` | body | `number` | no | Autotask opportunity advanced field 4. |
| `advancedField5` | body | `number` | no | Autotask opportunity advanced field 5. |
| `userDefinedFields[]` | body | `array<object>` | no | Optional Autotask opportunity user-defined fields. Multi-select and reference UDFs are not supported by the REST API. |
| `userDefinedFields[].name` | body | `string` | no | The exact name of the Autotask user-defined field. |
| `userDefinedFields[].value` | body | `string` | no | The user-defined field value. |
