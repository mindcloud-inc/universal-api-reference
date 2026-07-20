# Environmental Protection Agency: Get Annual Data By State

Retrieves annual summary data for a state from EPA AQS.

```
GET https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-annual-data-by-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Environmental Protection Agency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-annual-data-by-state?connectionId=$CONNECTION_ID&param=44201&bdate=20170101&edate=20171231&state=37" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-annual-data-by-state?${params}`, {
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
      "arithmetic_mean": 1,
      "cbsa": "string",
      "cbsa_code": "string",
      "certification_indicator": "string",
      "city": "string",
      "county": 1,
      "county_code": "string",
      "date_of_last_change": "2026-05-07T12:00:00.000Z",
      "datum": "string",
      "event_type": "string",
      "exceptional_data_count": 1,
      "fiftieth_percentile": 1,
      "first_max_datetime": "2026-05-07T12:00:00.000Z",
      "first_max_n_o_datetime": "2026-05-07T12:00:00.000Z",
      "first_max_nonoverlap_value": 1,
      "first_max_value": 1,
      "fourth_max_datetime": "2026-05-07T12:00:00.000Z",
      "fourth_max_value": 1,
      "latitude": 1,
      "local_site_name": "Ava Chen",
      "longitude": 1,
      "method": "string",
      "metric_used": "string",
      "ninetieth_percnetile": "string",
      "ninety_eigth_percentile": 1,
      "ninety_ninth_percentile": 1,
      "niney_fifth_percentile": 1,
      "null_observation_count": 1,
      "observation_count": 1,
      "observation_percent": 1,
      "parameter": "string",
      "parameter_code": "string",
      "poc": 1,
      "pollutant_standard": "string",
      "primary_exceedance_count": 1,
      "required_day_count": 1,
      "sample_duration": "string",
      "second_max_datetime": "2026-05-07T12:00:00.000Z",
      "second_max_n_o_datetime": "2026-05-07T12:00:00.000Z",
      "second_max_nonoverlap_value": 1,
      "second_max_value": 1,
      "secondary_exceedance_count": 1,
      "seventy_fifth_percentile": 1,
      "site_address": "string",
      "site_number": "string",
      "standard_deviation": 1,
      "state": "string",
      "state_code": "string",
      "tenth_percentile": 1,
      "third_max_datetime": "2026-05-07T12:00:00.000Z",
      "third_max_value": 1,
      "units_of_mesure": "string",
      "valid_day_count": 1,
      "validity_indicator": "string",
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arithmetic_mean` | number | The measure of central tendency obtained from the sum of the observed pollutant data values or National Ambient Air Quality Standards (NAAQS) averages in the yearly data set divided by the number of values that comprise the sum for the yearly data set. For criteria pollutants, the sum of values only adds the values with the appropriate flagging and concurrence for the exceptional data type. |
| `cbsa` | string | The shortened name of the core based statistical area (metropolitan area) where the monitoring site is located. |
| `cbsa_code` | string | The code of the core based statistical area (metropolitan area) where the monitoring site is located. |
| `certification_indicator` | string | An indication whether the completeness and accuracy of the reported monitoring information for a particular calendar year. Certified means the submitter has certified the data as complete and correct. Certification of a calendar year of data is due May 01 the year after collection. Certification not required means that the parameter does not require certification or the deadline has not yet passed. Uncertified (past due) means that certification is required but is overdue. Requested but not yet |
| `city` | string | The name of the city where the monitoring site is located. This represents the legal incorporated boundaries of cities and not urban areas. |
| `county` | number | The name of the county where the monitoring site is located. |
| `county_code` | string | A Federal Information Processing Standards (FIPS) code that identifies a county, parish, or independent city within a state. In certain cases other geo-political entities, such as tribe via the BIA tribal code, may be used. For border sites, it identifies the geo-political equivalent to U. S. states, such as Mexican states or Canadian provinces. When submitting transactions, a user may opt to use a Bureau of Indian Affairs tribal code in this fied (if the State Code was entered as 'TT' to indica |
| `date_of_last_change` | date | This represents the date the most relevant underlying data in AQS was last changed. That is, for annual summary data, it is the date these values were last affected by a change in raw data. If the AQCR code on the annual summary view changed, the date of last change would not be updated. |
| `datum` | string | The Datum associated with the Latitude and Longitude measures. The Datum represents the physical model of the earth used when determining latitude and longitude. AQS computes a "standard" location representation for all site location/coordinates so that data from AQS can be more easily used for mapping and geospatial analysis. This is accomplished using a geodatabase lookup to convert the user-provided coordinates into Latitude and Longitude with the standard horizontal datum of WGS84. (i.e. Thi |
| `event_type` | string | Indicates whether data measured during exceptional events are included in the summary. A wildfire is an example of an exceptional event; it is something that affects air quality, but the local agency has no control over. No Events means no events occurred. Events Included means events occurred and the data from them is included in the summary. Events Excluded means that events occurred but data form them is excluded from the summary. Concurred Events Excluded means that events occurred but only |
| `exceptional_data_count` | number | The number of data points in the annual data set affected by exceptional air quality events (things outside the norm that affect air quality). |
| `fiftieth_percentile` | number | The sample value in the summarized sample set where 50% of the values in that set are less than or equal to it. (For ozone, based on valid daily maxima; for PM2.5, based on seasonal and non-seasonal algorithms.) |
| `first_max_datetime` | date | The date and time (on a 24-hour clock) when the highest value for the year was taken. |
| `first_max_n_o_datetime` | date | The date and time (on a 24-hour clock) when the first maximum non overlapping value for the year was taken. |
| `first_max_nonoverlap_value` | number | For 8-hour CO averages, the highest value of the year. |
| `first_max_value` | number | The highest value for the indicated year. This only includes data at the selected duration or standard (e.g., it may be the maximum daily value). For seasonal monitoring, it only includes data during the effective monitoring season. |
| `fourth_max_datetime` | date | The date and time (on a 24-hour clock) when the fourth highest value for the year was taken. |
| `fourth_max_value` | number | The fourth highest value for the indicated year. This only includes data at the selected duration or standard (e.g., it may be the fourth maximum daily value). For seasonal monitoring, it only includes data during the effective monitoring season. |
| `latitude` | number | The angular distance north or south of the equator measured in decimal degrees. North is positive. AQS converts reported coordinates (latitude and longitude) to the same datum so that sites can be more easily used for mapping and geospatial analysis. The standard datum is WGS84 and this is the latitude in the WGS84 datum. |
| `local_site_name` | string | The identifier of the site in the onwning agency's (e.g., not US EPA) nomenclature. AQS makes no use of this field, but provides it on some output for the convenience of users. |
| `longitude` | number | The angular distance east or west of the prime meridian measured in decimal degrees. East is positive, West is negative. AQS converts reported coordinates (latitude and longitude) to the same datum so that sites can be more easily used for mapping and geospatial analysis. The standard datum is WGS84 and this is the longitude in the WGS84 datum. |
| `method` | string | A short description of the processes, equipment, and protocols used in gathering and measuring the sample. This field is a concatenation of the method of collection and the method of analysis. |
| `metric_used` | string | The base metric used in the calculation of the aggregate statistics presented in the remainder of the row. This corresponds to a form of a pollutant standard. For example, if this is Daily Maximum, then the value in the Mean column is the mean of the daily maximums. |
| `ninetieth_percnetile` | string | The sample value in the summarized sample set where 90% of the values in that set are less than or equal to it. (For ozone, based on valid daily maxima; for PM2.5, based on seasonal and non-seasonal algorithms.) |
| `ninety_eigth_percentile` | number | The sample value in the summarized sample set where 98% of the values in that set are less than or equal to it. (For ozone, based on valid daily maxima; for PM2.5, based on seasonal and non-seasonal algorithms.) |
| `ninety_ninth_percentile` | number | The sample value in the summarized sample set where 99% of the values in that set are less than or equal to it. (For ozone, based on valid daily maxima; for PM2.5, based on seasonal and non-seasonal algorithms.) |
| `niney_fifth_percentile` | number | The sample value in the summarized sample set where 95% of the values in that set are less than or equal to it. (For ozone, based on valid daily maxima; for PM2.5, based on seasonal and non-seasonal algorithms.) |
| `null_observation_count` | number | When a monitor does not make a scheduled sample, it should report a "null data reason code". This is the count of null data codes reported during the summary period. |
| `observation_count` | number | The number of observations (samples) taken during the averaging period. |
| `observation_percent` | number | The percent representing the number of observations taken with respect to the number scheduled to be taken during the aggregation period. This is only calculated for monitors where measurements are required (e.g., only certain parameters). |
| `parameter` | string | The name or description assigned in AQS to the parameter measured by the monitor. Parameters may be pollutants or non-pollutants (e.g., wind speed). |
| `parameter_code` | string | The AQS code corresponding to the parameter measured by the monitor. |
| `poc` | number | This is the "Parameter Occurrence Code" used to distinguish different instruments that measure the same parameter at the same site. There is no meaning to the POC (e.g. POC 1 does not indicate the primary monitor). For example, the first monitor established to measure carbon monoxide (CO) at a site could have a POC of 1. If an additional monitor were established at the same site to measure CO, that monitor could have a POC of 2. However, if a new instrument were installed to replace the original |
| `pollutant_standard` | string | A description of the national ambient air quality standard (NAAQS) rules used to calculate aggregate statistics. A pollutant standard will include the pollutant, the averaging time, and the year of promulgation. AQS calculates and stores aggregate information for the following current and some historical standards: ======================== =================== Pollutant Standard Name AQS Parameter Code ======================== =================== Lead Quarterly 1978 12128 Lead 3-Month (PM10) 2009 |
| `primary_exceedance_count` | number | The number of times during the year the pollutant levels (expressed in the NAAQS average) exceeded the NAAQS standard. |
| `required_day_count` | number | The number of days during the year which the monitor was scheduled to take samples if measurements are required. |
| `sample_duration` | string | The length of time that air passes through the monitoring device before it is analyzed (measured). So, it represents an averaging period in the atmosphere (for example, a 24-hour sample duration draws ambient air over a collection filter for 24 straight hours). For continuous monitors, it can represent an averaging time of many samples (for example, a 1-hour value may be the average of four one-minute samples collected during each quarter of the hour). There are two types of sample durations. Fi |
| `second_max_datetime` | date | The date and time (on a 24-hour clock) when the second highest value for the year was taken. |
| `second_max_n_o_datetime` | date | The date and time (on a 24-hour clock) when the second maximum non overlapping value for the year was taken. |
| `second_max_nonoverlap_value` | number | For 8-hour CO averages, the second highest value of the year that does not share any hours with the 8-hour period of the first max non overlapping value. |
| `second_max_value` | number | The second highest value for the indicated year. This only includes data at the selected duration or standard (e.g., it may be the second maximum daily value). For seasonal monitoring, it only includes data during the effective monitoring season. |
| `secondary_exceedance_count` | number | The number of samples during the year that exceeded the secondary air quality standard. |
| `seventy_fifth_percentile` | number | The sample value in the summarized sample set where 75% of the values in that set are less than or equal to it. (For ozone, based on valid daily maxima; for PM2.5, based on seasonal and non-seasonal algorithms.) |
| `site_address` | string | The street address giving an approximate location (building number and street; or other descriptor) of the site. |
| `site_number` | string | The 4-digit number used to uniquely identify the air monitoring site within a county or tribal land. The values are always numeric, but are treated as a string and padded with leading zeroes so they must always have 4 digits. There is no requirement that Site Numbers be assigned continuously or in any particular order. Regional or local organizations are thus free to allocate Site Numbers in any way they choose, as long as there is no duplication within a county or tribal area. Be aware that a t |
| `standard_deviation` | number | The standard deviation about the mean of the values for the averaging period. This value is a measure of the dispersion about the central tendency of a pollutant that is the square root of the precision mean of the squares of the variation of each Relative Percent Differences of a value pair from the precision mean of the Relative Percent Differences of the value pairs for the time period. Used in monitor precision (summary) calculations and agency level calculations. |
| `state` | string | The name of the state where the monitoring site is located. |
| `state_code` | string | The FIPS code of the state in which the monitor resides. AQS uses 2-digit or character codes that identifies one of the 50 states, U. S. territories, or Washington, DC. For border sites, the code '80' is used for Mexico and 'CC' is used for Canada. When submitting transactions, a user may opt to use the code 'TT' to indicate that this data is for a Native American Tribe, and that the next field on the transaction identifies a tribal area using the Bureau of Indian Affairs tribal code. Data in th |
| `tenth_percentile` | number | The sample value in the summarized sample set where 10% of the values in that set are less than or equal to it. (For ozone, based on valid daily maxima; for PM2.5, based on seasonal and non-seasonal algorithms.) |
| `third_max_datetime` | date | The date and time (on a 24-hour clock) when the third highest value for the year was taken. |
| `third_max_value` | number | The third highest value for the indicated year. This only includes data at the selected duration or standard (e.g., it may be the third maximum daily value). For seasonal monitoring, it only includes data during the effective monitoring season. |
| `units_of_mesure` | string | The unit of measure for all statistics on the same row. Every parameter has a standard unit of measure. Submitters are allowed to report data in any unit and EPA converts to a standard unit so that we may use the data in calculations. |
| `valid_day_count` | number | The number of required monitoring days in the aggregation period (e.g., year) where the monitoring criteria were met. (Only applicable for criteria pollutants.) |
| `validity_indicator` | string | An indicator whether the calculated value meets all completeness criteria to be considered valid. |
| `year` | number | The year the data represents. |

## Native endpoint

Through the native Environmental Protection Agency API, this operation is `GET /annualData/byState` (base URL `https://aqs.epa.gov/data/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-annual-data-by-state.md) for the provider-specific parameters and requirements.

