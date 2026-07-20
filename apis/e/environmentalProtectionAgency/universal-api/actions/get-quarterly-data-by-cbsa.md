# Environmental Protection Agency: Get Quarterly Data By CBSA

Retrieves quarterly summary data for a CBSA from EPA AQS.

```
GET https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-quarterly-data-by-cbsa
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Environmental Protection Agency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-quarterly-data-by-cbsa?connectionId=$CONNECTION_ID&param=44201&bdate=20170101&edate=20171231&cbsa=16740" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "param": "44201",
  "bdate": "20170101",
  "edate": "20171231",
  "cbsa": "16740"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-quarterly-data-by-cbsa?${params}`, {
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
| `cbsa` | string | yes | Five-digit Core Based Statistical Area code. Example: `16740`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cbdate` | string | no | Optional begin date in YYYYMMDD format for filtering by date of last change. Example: `20180101`. |
| `cedate` | string | no | Optional end date in YYYYMMDD format for filtering by date of last change. Example: `20181231`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actual_days_gt_std": 1,
      "address": "string",
      "arithmetic_mean": 1,
      "cbsa_code": "string",
      "cbsa_name": "Ava Chen",
      "city": "string",
      "county": 1,
      "county_code": "string",
      "date_of_last_change": "2026-05-07T12:00:00.000Z",
      "datum": "string",
      "estimated_days_gt_std": 1,
      "event_type": "string",
      "latitude": 1,
      "local_site_name": "Ava Chen",
      "longitude": 1,
      "maximum_value": 1,
      "minimum_value": 1,
      "monitoring_agency": "string",
      "monitoring_agency_code": "string",
      "observation_count": 1,
      "observation_percent": 1,
      "parameter": "string",
      "parameter_code": "string",
      "percent_days": 1,
      "percent_one_value": 1,
      "poc": 1,
      "pollutant_standard": "string",
      "quarter": 1,
      "quarterly_criteria_met": "string",
      "sample_duration": "string",
      "sample_duration_code": "string",
      "sample_duration_type": "string",
      "scheduled_samples": 1,
      "site_number": "string",
      "state": "string",
      "state_code": "string",
      "tribal_code": "string",
      "tribal_land": "string",
      "units_of_measure": "string",
      "valid_day_count": 1,
      "valid_samples": 1,
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actual_days_gt_std` | number | The number of days during the year that exceeded the standard (as opposed to estimated days). |
| `address` | string | The street address giving an approximate location (building number and street; or other descriptor) of the site. |
| `arithmetic_mean` | number | The measure of central tendency obtained from the sum of the observed pollutant data values in the quarterly data set divided by the number of values that comprise the sum for the quarterly data set. For criteria pollutants, the sum of values only adds the values with the appropriate flagging and concurrence for the exceptional data type. |
| `cbsa_code` | string | The code of the core based statistical area (metropolitan area) where the monitoring site is located. |
| `cbsa_name` | string | The shortened name of the core based statistical area (metropolitan area) where the monitoring site is located. |
| `city` | string | The name of the city where the monitoring site is located. This represents the legal incorporated boundaries of cities and not urban areas. |
| `county` | number | The name of the county where the monitoring site is located. |
| `county_code` | string | A Federal Information Processing Standards (FIPS) code that identifies a county, parish, or independent city within a state. In certain cases other geo-political entities, such as tribe via the BIA tribal code, may be used. For border sites, it identifies the geo-political equivalent to U. S. states, such as Mexican states or Canadian provinces. When submitting transactions, a user may opt to use a Bureau of Indian Affairs tribal code in this fied (if the State Code was entered as 'TT' to indica |
| `date_of_last_change` | date | This represents the date the most relevant underlying data in AQS was last changed. That is, for annual summary data, it is the date these values were last affected by a change in raw data. If the AQCR code on the annual summary view changed, the date of last change would not be updated. |
| `datum` | string | The Datum associated with the Latitude and Longitude measures. The Datum represents the physical model of the earth used when determining latitude and longitude. AQS computes a "standard" location representation for all site location/coordinates so that data from AQS can be more easily used for mapping and geospatial analysis. This is accomplished using a geodatabase lookup to convert the user-provided coordinates into Latitude and Longitude with the standard horizontal datum of WGS84. (i.e. Thi |
| `estimated_days_gt_std` | number | The estimated number of days greater than the standard for the year (or quarter if viewing quarterly data). It is computed for specific pollutants when an exceedance has occurred during the year. The underlying assumption is that missing data is just as likely to exceed the standard as reported data. |
| `event_type` | string | Indicates whether data measured during exceptional events are included in the summary. A wildfire is an example of an exceptional event; it is something that affects air quality, but the local agency has no control over. No Events means no events occurred. Events Included means events occurred and the data from them is included in the summary. Events Excluded means that events occurred but data form them is excluded from the summary. Concurred Events Excluded means that events occurred but only |
| `latitude` | number | The angular distance north or south of the equator measured in decimal degrees. North is positive. AQS converts reported coordinates (latitude and longitude) to the same datum so that sites can be more easily used for mapping and geospatial analysis. The standard datum is WGS84 and this is the latitude in the WGS84 datum. |
| `local_site_name` | string | The identifier of the site in the onwning agency's (e.g., not US EPA) nomenclature. AQS makes no use of this field, but provides it on some output for the convenience of users. |
| `longitude` | number | The angular distance east or west of the prime meridian measured in decimal degrees. East is positive, West is negative. AQS converts reported coordinates (latitude and longitude) to the same datum so that sites can be more easily used for mapping and geospatial analysis. The standard datum is WGS84 and this is the longitude in the WGS84 datum. |
| `maximum_value` | number | The maximum value for the year at the given duration for the aggregation period. Sometimes the Nth maximum value is labelled. This would be the rank order value in that position meeting the criteria given below. For example, the 4th maximum value would be the 4th in the rank ordered set. |
| `minimum_value` | number | The lowest sample value recorded during the aggregation period. |
| `monitoring_agency` | string | The name of the agency responsible for operating the monitor. |
| `monitoring_agency_code` | string | The code representing the agency responsible for operating the monitor. |
| `observation_count` | number | The number of observations (samples) taken during the averaging period. |
| `observation_percent` | number | The percent representing the number of observations taken with respect to the number scheduled to be taken during the aggregation period. This is only calculated for monitors where measurements are required (e.g., only certain parameters). |
| `parameter` | string | The name or description assigned in AQS to the parameter measured by the monitor. Parameters may be pollutants or non-pollutants (e.g., wind speed). |
| `parameter_code` | string | The AQS code corresponding to the parameter measured by the monitor. |
| `percent_days` | number | Percent Days is the percentage of valid days in a quarter compared to the total number of days in the quarter. In all equations below the valid day count is the number of daily summaries, with the corresponding pollutant standard and exceptional data type, where the summary criterion is met. |
| `percent_one_value` | number | Percentage of days with at least one sample measurement (ignoring flagging and concurrence). |
| `poc` | number | This is the "Parameter Occurrence Code" used to distinguish different instruments that measure the same parameter at the same site. There is no meaning to the POC (e.g. POC 1 does not indicate the primary monitor). For example, the first monitor established to measure carbon monoxide (CO) at a site could have a POC of 1. If an additional monitor were established at the same site to measure CO, that monitor could have a POC of 2. However, if a new instrument were installed to replace the original |
| `pollutant_standard` | string | A description of the national ambient air quality standard (NAAQS) rules used to calculate aggregate statistics. A pollutant standard will include the pollutant, the averaging time, and the year of promulgation. AQS calculates and stores aggregate information for the following current and some historical standards: ======================== =================== Pollutant Standard Name AQS Parameter Code ======================== =================== Lead Quarterly 1978 12128 Lead 3-Month (PM10) 2009 |
| `quarter` | number | Number (1-4) of the calendar quarter in the year to which the data applies. For example, the quarter in which the first exceedance occurred. |
| `quarterly_criteria_met` | string | An indicator that the quarterly data completeness criteria were met by the monitor. |
| `sample_duration` | string | The length of time that air passes through the monitoring device before it is analyzed (measured). So, it represents an averaging period in the atmosphere (for example, a 24-hour sample duration draws ambient air over a collection filter for 24 straight hours). For continuous monitors, it can represent an averaging time of many samples (for example, a 1-hour value may be the average of four one-minute samples collected during each quarter of the hour). There are two types of sample durations. Fi |
| `sample_duration_code` | string | A code representing the Sample Duration (the length of time the sample represents; the averaging time). The code does not necessarily correspond to a real world value (e.g., "5" is not for a 5 hour sample duration). |
| `sample_duration_type` | string | An indicator of whether the duration is a reported "raw" (observed) duration or an AQS calculated aggregate duration. |
| `scheduled_samples` | number | The count of sample measurements that were taken on scheduled sample dates during the indicated time period (quarter or year). |
| `site_number` | string | The 4-digit number used to uniquely identify the air monitoring site within a county or tribal land. The values are always numeric, but are treated as a string and padded with leading zeroes so they must always have 4 digits. There is no requirement that Site Numbers be assigned continuously or in any particular order. Regional or local organizations are thus free to allocate Site Numbers in any way they choose, as long as there is no duplication within a county or tribal area. Be aware that a t |
| `state` | string | The name of the state where the monitoring site is located. |
| `state_code` | string | The FIPS code of the state in which the monitor resides. AQS uses 2-digit or character codes that identifies one of the 50 states, U. S. territories, or Washington, DC. For border sites, the code '80' is used for Mexico and 'CC' is used for Canada. When submitting transactions, a user may opt to use the code 'TT' to indicate that this data is for a Native American Tribe, and that the next field on the transaction identifies a tribal area using the Bureau of Indian Affairs tribal code. Data in th |
| `tribal_code` | string | The BIA code representing the tribe on whose land the monitoring site resides. This is an optional way of displaying data. A tribe may (or may not) chose to enter their site's geographic location data using tribal code (rather than a state and county code). |
| `tribal_land` | string | The BIA name of the tribe with responsibility for operating the monitor, reporting data, etc. |
| `units_of_measure` | string | The unit of measure for all statistics on the same row. Every parameter has a standard unit of measure. Submitters are allowed to report data in any unit and EPA converts to a standard unit so that we may use the data in calculations. |
| `valid_day_count` | number | The number of required monitoring days in the aggregation period (e.g., year) where the monitoring criteria were met. (Only applicable for criteria pollutants.) |
| `valid_samples` | number | The total number of observations that meet minimum threshold requirements. |
| `year` | number | The year the data represents. |

## Native endpoint

Through the native Environmental Protection Agency API, this operation is `GET /quarterlyData/byCBSA` (base URL `https://aqs.epa.gov/data/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quarterly-data-by-cbsa.md) for the provider-specific parameters and requirements.

