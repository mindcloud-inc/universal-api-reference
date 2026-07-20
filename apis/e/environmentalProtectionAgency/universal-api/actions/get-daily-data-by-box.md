# Environmental Protection Agency: Get Daily Data By Box

Retrieves daily summary data for a bounding box from EPA AQS.

```
GET https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-daily-data-by-box
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Environmental Protection Agency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-daily-data-by-box?connectionId=$CONNECTION_ID&param=44201&bdate=20170101&edate=20171231&minlat=33.3&maxlat=33.6&minlon=-87.0&maxlon=-86.7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "param": "44201",
  "bdate": "20170101",
  "edate": "20171231",
  "minlat": "33.3",
  "maxlat": "33.6",
  "minlon": "-87.0",
  "maxlon": "-86.7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-daily-data-by-box?${params}`, {
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
| `minlat` | number | yes | Southern latitude bound for a geographic box query. Example: `33.3`. |
| `maxlat` | number | yes | Northern latitude bound for a geographic box query. Example: `33.6`. |
| `minlon` | number | yes | Western longitude bound for a geographic box query. Use negative values in the western hemisphere. Example: `-87.0`. |
| `maxlon` | number | yes | Eastern longitude bound for a geographic box query. Use negative values in the western hemisphere. Example: `-86.7`. |

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
      "aqi": 1,
      "arithmetic_mean": 1,
      "cbsa": "string",
      "cbsa_code": "string",
      "city": "string",
      "county": 1,
      "county_code": "string",
      "date_local": "2026-05-07T12:00:00.000Z",
      "date_of_last_change": "2026-05-07T12:00:00.000Z",
      "datum": "string",
      "event_type": "string",
      "first_max_hour": 1,
      "first_max_value": 1,
      "latitude": 1,
      "local_site_name": "Ava Chen",
      "longitude": 1,
      "method": "string",
      "method_code": "string",
      "observation_count": 1,
      "observation_percent": 1,
      "parameter": "string",
      "parameter_code": "string",
      "poc": 1,
      "pollutant_standard": "string",
      "sample_duration": "string",
      "site_address": "string",
      "site_number": "string",
      "state": "string",
      "state_code": "string",
      "units_of_measure": "string",
      "validity_indicator": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aqi` | number | The Air Quality Index for the day for the pollutant, if applicable. The air quality index is a unitless measure of the amount of pollutant that can be used to relate the pollutant to the healthy levels and indicate possible health concerns with elevated levels. The Air Quality Index (AQI) is a measure for reporting daily air quality. It focuses on health effects that may be experienced within a few hours or days after breathing polluted air. AQI is calculated for the following major air pollutan |
| `arithmetic_mean` | number | The measure of central tendency obtained from the sum of the observed pollutant data values or National Ambient Air Quality Standards (NAAQS) averages in the daily data set divided by the number of values that comprise the sum for the daily data set. For criteria pollutants, the sum of values only adds the values with the appropriate flagging and concurrence for the exceptional data type. |
| `cbsa` | string | The shortened name of the core based statistical area (metropolitan area) where the monitoring site is located. |
| `cbsa_code` | string | The code of the core based statistical area (metropolitan area) where the monitoring site is located. |
| `city` | string | The name of the city where the monitoring site is located. This represents the legal incorporated boundaries of cities and not urban areas. |
| `county` | number | The name of the county where the monitoring site is located. |
| `county_code` | string | A Federal Information Processing Standards (FIPS) code that identifies a county, parish, or independent city within a state. In certain cases other geo-political entities, such as tribe via the BIA tribal code, may be used. For border sites, it identifies the geo-political equivalent to U. S. states, such as Mexican states or Canadian provinces. When submitting transactions, a user may opt to use a Bureau of Indian Affairs tribal code in this fied (if the State Code was entered as 'TT' to indica |
| `date_local` | date | The date the sample was taken in Local Standard Time. This represents only the date, the time is in a separate field. This time reflects the beginning of the sample duration. That is, if the time is 2:00 and the duration is 1-hour, then sampling happened from 2:00 - 3:00. |
| `date_of_last_change` | date | This represents the date the most relevant underlying data in AQS was last changed. That is, for annual summary data, it is the date these values were last affected by a change in raw data. If the AQCR code on the annual summary view changed, the date of last change would not be updated. |
| `datum` | string | The Datum associated with the Latitude and Longitude measures. The Datum represents the physical model of the earth used when determining latitude and longitude. AQS computes a "standard" location representation for all site location/coordinates so that data from AQS can be more easily used for mapping and geospatial analysis. This is accomplished using a geodatabase lookup to convert the user-provided coordinates into Latitude and Longitude with the standard horizontal datum of WGS84. (i.e. Thi |
| `event_type` | string | Indicates whether data measured during exceptional events are included in the summary. A wildfire is an example of an exceptional event; it is something that affects air quality, but the local agency has no control over. No Events means no events occurred. Events Included means events occurred and the data from them is included in the summary. Events Excluded means that events occurred but data form them is excluded from the summary. Concurred Events Excluded means that events occurred but only |
| `first_max_hour` | number | The time (on a 24-hour clock) when the highest value for the day was taken. |
| `first_max_value` | number | The highest value for the indicated year. This only includes data at the selected duration or standard (e.g., it may be the maximum daily value). For seasonal monitoring, it only includes data during the effective monitoring season. |
| `latitude` | number | The angular distance north or south of the equator measured in decimal degrees. North is positive. AQS converts reported coordinates (latitude and longitude) to the same datum so that sites can be more easily used for mapping and geospatial analysis. The standard datum is WGS84 and this is the latitude in the WGS84 datum. |
| `local_site_name` | string | The identifier of the site in the onwning agency's (e.g., not US EPA) nomenclature. AQS makes no use of this field, but provides it on some output for the convenience of users. |
| `longitude` | number | The angular distance east or west of the prime meridian measured in decimal degrees. East is positive, West is negative. AQS converts reported coordinates (latitude and longitude) to the same datum so that sites can be more easily used for mapping and geospatial analysis. The standard datum is WGS84 and this is the longitude in the WGS84 datum. |
| `method` | string | A short description of the processes, equipment, and protocols used in gathering and measuring the sample. This field is a concatenation of the method of collection and the method of analysis. |
| `method_code` | string | A three-digit code representing the measurement method. A method code is only unique within a parameter (that is, method 132 for ozone is not the same as method 123 for benzene). The encoding contains both the sample collection and sample analysis descriptions. |
| `observation_count` | number | The number of observations (samples) taken during the averaging period. |
| `observation_percent` | number | The percent of sample values that were reported compared to the number of data values scheduled to have been reported for the 24-hour (midnight to midnight local time) period. For observed durations, this includes only non-null values (e.g., actual samples). For NAAQS durations (e.g., 8-Hour ozone) this includes the number calculated NAAQS durations summaries. |
| `parameter` | string | The name or description assigned in AQS to the parameter measured by the monitor. Parameters may be pollutants or non-pollutants (e.g., wind speed). |
| `parameter_code` | string | The AQS code corresponding to the parameter measured by the monitor. |
| `poc` | number | This is the "Parameter Occurrence Code" used to distinguish different instruments that measure the same parameter at the same site. There is no meaning to the POC (e.g. POC 1 does not indicate the primary monitor). For example, the first monitor established to measure carbon monoxide (CO) at a site could have a POC of 1. If an additional monitor were established at the same site to measure CO, that monitor could have a POC of 2. However, if a new instrument were installed to replace the original |
| `pollutant_standard` | string | A description of the national ambient air quality standard (NAAQS) rules used to calculate aggregate statistics. A pollutant standard will include the pollutant, the averaging time, and the year of promulgation. AQS calculates and stores aggregate information for the following current and some historical standards: ======================== =================== Pollutant Standard Name AQS Parameter Code ======================== =================== Lead Quarterly 1978 12128 Lead 3-Month (PM10) 2009 |
| `sample_duration` | string | The length of time that air passes through the monitoring device before it is analyzed (measured). So, it represents an averaging period in the atmosphere (for example, a 24-hour sample duration draws ambient air over a collection filter for 24 straight hours). For continuous monitors, it can represent an averaging time of many samples (for example, a 1-hour value may be the average of four one-minute samples collected during each quarter of the hour). There are two types of sample durations. Fi |
| `site_address` | string | The street address giving an approximate location (building number and street; or other descriptor) of the site. |
| `site_number` | string | The 4-digit number used to uniquely identify the air monitoring site within a county or tribal land. The values are always numeric, but are treated as a string and padded with leading zeroes so they must always have 4 digits. There is no requirement that Site Numbers be assigned continuously or in any particular order. Regional or local organizations are thus free to allocate Site Numbers in any way they choose, as long as there is no duplication within a county or tribal area. Be aware that a t |
| `state` | string | The name of the state where the monitoring site is located. |
| `state_code` | string | The FIPS code of the state in which the monitor resides. AQS uses 2-digit or character codes that identifies one of the 50 states, U. S. territories, or Washington, DC. For border sites, the code '80' is used for Mexico and 'CC' is used for Canada. When submitting transactions, a user may opt to use the code 'TT' to indicate that this data is for a Native American Tribe, and that the next field on the transaction identifies a tribal area using the Bureau of Indian Affairs tribal code. Data in th |
| `units_of_measure` | string | The unit of measure for all statistics on the same row. Every parameter has a standard unit of measure. Submitters are allowed to report data in any unit and EPA converts to a standard unit so that we may use the data in calculations. |
| `validity_indicator` | string | An indicator whether the calculated value meets all completeness criteria to be considered valid. |

## Native endpoint

Through the native Environmental Protection Agency API, this operation is `GET /dailyData/byBox` (base URL `https://aqs.epa.gov/data/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-daily-data-by-box.md) for the provider-specific parameters and requirements.

