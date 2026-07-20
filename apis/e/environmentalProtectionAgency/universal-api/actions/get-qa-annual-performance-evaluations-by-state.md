# Environmental Protection Agency: Get QA Annual Performance Evaluations By State

Retrieves QA annual performance evaluations for a state from EPA AQS.

```
GET https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-qa-annual-performance-evaluations-by-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Environmental Protection Agency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-qa-annual-performance-evaluations-by-state?connectionId=$CONNECTION_ID&param=44201&bdate=20170101&edate=20171231&state=37" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "param": "44201",
  "bdate": "20170101",
  "edate": "20171231",
  "state": "37"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-qa-annual-performance-evaluations-by-state?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `param` | string | yes | AQS parameter code. EPA allows up to five comma-separated 5-digit parameter codes for most data services. Accepts multiple values in one string, delimited by `,`. Example: `44201`. |
| `bdate` | string | yes | Begin date in YYYYMMDD format. Example: `20170101`. |
| `edate` | string | yes | End date in YYYYMMDD format. EPA requires this to be in the same year as the begin date except for monitors. Example: `20171231`. |
| `state` | string | yes | Two-digit state FIPS code, including a leading zero when applicable. Example: `37`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "analyzing_agency": "string",
      "analyzing_agency_code": "string",
      "assessment_date": "2026-05-07T12:00:00.000Z",
      "assessmnet_number": 1,
      "auditing_agency": "string",
      "auditing_agency_code": "string",
      "cbsa_code": "string",
      "cbsa_name": "Ava Chen",
      "city_name": "Ava Chen",
      "county_code": "string",
      "county_name": 1,
      "csa_code": "string",
      "csa_name": "Ava Chen",
      "date_of_last_change": "2026-05-07T12:00:00.000Z",
      "datum": "string",
      "latitude": 1,
      "local_site_name": "Ava Chen",
      "longitude": 1,
      "lvl_1_assessment_concentration": 1,
      "lvl_1_monitor_concentration": 1,
      "lvl_10_assessment_concentration": 1,
      "lvl_10_monitor_concentration": 1,
      "lvl_2_assessment_concentration": 1,
      "lvl_2_monitor_concentration": 1,
      "lvl_3_assessment_concentration": 1,
      "lvl_3_monitor_concentration": 1,
      "lvl_4_assessment_concentration": 1,
      "lvl_4_monitor_concentration": 1,
      "lvl_5_assessment_concentration": 1,
      "lvl_5_monitor_concentration": 1,
      "lvl_6_assessment_concentration": 1,
      "lvl_6_monitor_concentration": 1,
      "lvl_7_assessment_concentration": 1,
      "lvl_7_monitor_concentration": 1,
      "lvl_8_assessment_concentration": 1,
      "lvl_8_monitor_concentration": 1,
      "lvl_9_assessment_concentration": 1,
      "lvl_9_monitor_concentration": 1,
      "method": "string",
      "method_code": "string",
      "monitoring_agency": "string",
      "monitoring_agency_code": "string",
      "parameter": "string",
      "parameter_code": "string",
      "performing_agency": "string",
      "performing_agency_code": "string",
      "poc": 1,
      "pqao": "string",
      "pqao_code": "string",
      "site_number": "string",
      "state_code": "string",
      "state_name": "Ava Chen",
      "tribal_code": "string",
      "tribe_name": "Ava Chen",
      "unit": "string",
      "unit_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | The street address giving an approximate location (building number and street; or other descriptor) of the site. |
| `analyzing_agency` | string | The name of the agency assigned as "Analyzing" for the monitor reporting data. |
| `analyzing_agency_code` | string | The code of the agency assigned as "Analyzing" for the monitor reporting data. |
| `assessment_date` | date | Date that the QA assessment was performed |
| `assessmnet_number` | number | A unique number associated with an assessment performed at a site on a given day. Value should be "1" unless additional same assessments are performed on the same day. |
| `auditing_agency` | string | The name of the agency assigned as "Auditing" for the monitor reporting data. |
| `auditing_agency_code` | string | The code of the agency assigned as "Auditing" for the monitor reporting data. |
| `cbsa_code` | string | The code of the core based statistical area (metropolitan area) where the monitoring site is located. |
| `cbsa_name` | string | The shortened name of the core based statistical area (metropolitan area) where the monitoring site is located. |
| `city_name` | string | The name of the city where the monitoring site is located. This represents the legal incorporated boundaries of cities and not urban areas. |
| `county_code` | string | A Federal Information Processing Standards (FIPS) code that identifies a county, parish, or independent city within a state. In certain cases other geo-political entities, such as tribe via the BIA tribal code, may be used. For border sites, it identifies the geo-political equivalent to U. S. states, such as Mexican states or Canadian provinces. When submitting transactions, a user may opt to use a Bureau of Indian Affairs tribal code in this fied (if the State Code was entered as 'TT' to indica |
| `county_name` | number | The name of the state where the monitoring site is located. |
| `csa_code` | string | The code of the combined statistical area where the monitoring site is located. |
| `csa_name` | string | The shortened name of the combined statistical area where the monitoring site is located. |
| `date_of_last_change` | date | This represents the date the most relevant underlying data in AQS was last changed. That is, for annual summary data, it is the date these values were last affected by a change in raw data. If the AQCR code on the annual summary view changed, the date of last change would not be updated. |
| `datum` | string | The Datum associated with the Latitude and Longitude measures. The Datum represents the physical model of the earth used when determining latitude and longitude. AQS computes a "standard" location representation for all site location/coordinates so that data from AQS can be more easily used for mapping and geospatial analysis. This is accomplished using a geodatabase lookup to convert the user-provided coordinates into Latitude and Longitude with the standard horizontal datum of WGS84. (i.e. Thi |
| `latitude` | number |  |
| `local_site_name` | string | The identifier of the site in the onwning agency's (e.g., not US EPA) nomenclature. AQS makes no use of this field, but provides it on some output for the convenience of users. |
| `longitude` | number |  |
| `lvl_1_assessment_concentration` | number |  |
| `lvl_1_monitor_concentration` | number |  |
| `lvl_10_assessment_concentration` | number |  |
| `lvl_10_monitor_concentration` | number |  |
| `lvl_2_assessment_concentration` | number |  |
| `lvl_2_monitor_concentration` | number |  |
| `lvl_3_assessment_concentration` | number |  |
| `lvl_3_monitor_concentration` | number |  |
| `lvl_4_assessment_concentration` | number |  |
| `lvl_4_monitor_concentration` | number |  |
| `lvl_5_assessment_concentration` | number |  |
| `lvl_5_monitor_concentration` | number |  |
| `lvl_6_assessment_concentration` | number |  |
| `lvl_6_monitor_concentration` | number |  |
| `lvl_7_assessment_concentration` | number |  |
| `lvl_7_monitor_concentration` | number |  |
| `lvl_8_assessment_concentration` | number |  |
| `lvl_8_monitor_concentration` | number |  |
| `lvl_9_assessment_concentration` | number |  |
| `lvl_9_monitor_concentration` | number |  |
| `method` | string | A short description of the processes, equipment, and protocols used in gathering and measuring the sample. This field is a concatenation of the method of collection and the method of analysis. |
| `method_code` | string | A three-digit code representing the measurement method. A method code is only unique within a parameter (that is, method 132 for ozone is not the same as method 123 for benzene). The encoding contains both the sample collection and sample analysis descriptions. |
| `monitoring_agency` | string | The name of the agency responsible for operating the monitor. |
| `monitoring_agency_code` | string | The code representing the agency responsible for operating the monitor. |
| `parameter` | string | The name or description assigned in AQS to the parameter measured by the monitor. Parameters may be pollutants or non-pollutants (e.g., wind speed). |
| `parameter_code` | string | The AQS code corresponding to the parameter measured by the monitor. |
| `performing_agency` | string | The name of the Agency or organization performing the quality assurance assessment. |
| `performing_agency_code` | string | A code representing the Agency or organization performing the quality assurance assessment. |
| `poc` | number | This is the "Parameter Occurrence Code" used to distinguish different instruments that measure the same parameter at the same site. There is no meaning to the POC (e.g. POC 1 does not indicate the primary monitor). For example, the first monitor established to measure carbon monoxide (CO) at a site could have a POC of 1. If an additional monitor were established at the same site to measure CO, that monitor could have a POC of 2. However, if a new instrument were installed to replace the original |
| `pqao` | string | The name of the agency assigned as Primary Quality Assurance Organization for the monitor reporting data. |
| `pqao_code` | string | The code representing the Primary Quality Assurance Organization for this monitor. |
| `site_number` | string | The 4-digit number used to uniquely identify the air monitoring site within a county or tribal land. The values are always numeric, but are treated as a string and padded with leading zeroes so they must always have 4 digits. There is no requirement that Site Numbers be assigned continuously or in any particular order. Regional or local organizations are thus free to allocate Site Numbers in any way they choose, as long as there is no duplication within a county or tribal area. Be aware that a t |
| `state_code` | string | The FIPS code of the state in which the monitor resides. AQS uses 2-digit or character codes that identifies one of the 50 states, U. S. territories, or Washington, DC. For border sites, the code '80' is used for Mexico and 'CC' is used for Canada. When submitting transactions, a user may opt to use the code 'TT' to indicate that this data is for a Native American Tribe, and that the next field on the transaction identifies a tribal area using the Bureau of Indian Affairs tribal code. Data in th |
| `state_name` | string | The name of the state where the monitoring site is located. |
| `tribal_code` | string | The BIA code representing the tribe on whose land the monitoring site resides. This is an optional way of displaying data. A tribe may (or may not) chose to enter their site's geographic location data using tribal code (rather than a state and county code). |
| `tribe_name` | string | The BIA name of the tribe with responsibility for operating the monitor, reporting data, etc. |
| `unit` | string | The unit of measure for all statistics on the same row. Every parameter has a standard unit of measure. Submitters are allowed to report data in any unit and EPA converts to a standard unit so that we may use the data in calculations. |
| `unit_code` | string | A code representing the units of measure. |

## Native endpoint

Through the native Environmental Protection Agency API, this operation is `GET /qaAnnualPerformanceEvaluations/byState` (base URL `https://aqs.epa.gov/data/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-qa-annual-performance-evaluations-by-state.md) for the provider-specific parameters and requirements.

