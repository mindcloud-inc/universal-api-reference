# Environmental Protection Agency: Get Sample Data By Box

Retrieves sample data for a bounding box from EPA AQS.

```
GET https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-sample-data-by-box
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Environmental Protection Agency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-sample-data-by-box?connectionId=$CONNECTION_ID&param=44201&bdate=20170101&edate=20171231&minlat=33.3&maxlat=33.6&minlon=-87.0&maxlon=-86.7" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-sample-data-by-box?${params}`, {
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
| `duration` | string | no | Optional one-character AQS sample duration code for sample data requests. Example: `1`. |
| `cbdate` | string | no | Optional begin date in YYYYMMDD format for filtering by date of last change. Example: `20180101`. |
| `cedate` | string | no | Optional end date in YYYYMMDD format for filtering by date of last change. Example: `20181231`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cbsa_code": "string",
      "county": 1,
      "county_code": "string",
      "date_gmt": "2026-05-07T12:00:00.000Z",
      "date_local": "2026-05-07T12:00:00.000Z",
      "date_of_last_change": "2026-05-07T12:00:00.000Z",
      "datum": "string",
      "detection_limit": 1,
      "latitude": 1,
      "longitude": 1,
      "method": "string",
      "method_code": "string",
      "method_type": "string",
      "parameter": "string",
      "parameter_code": "string",
      "poc": 1,
      "qualifiers": "string",
      "sample_duration": "string",
      "sample_frequency": "string",
      "sample_measurement": "string",
      "site_number": "string",
      "state": "string",
      "state_code": "string",
      "time_gmt": "string",
      "time_local": "string",
      "uncertainty": 1,
      "units_of_measure": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cbsa_code` | string | The code of the core based statistical area (metropolitan area) where the monitoring site is located. |
| `county` | number | The name of the county where the monitoring site is located. |
| `county_code` | string | A Federal Information Processing Standards (FIPS) code that identifies a county, parish, or independent city within a state. In certain cases other geo-political entities, such as tribe via the BIA tribal code, may be used. For border sites, it identifies the geo-political equivalent to U. S. states, such as Mexican states or Canadian provinces. When submitting transactions, a user may opt to use a Bureau of Indian Affairs tribal code in this fied (if the State Code was entered as 'TT' to indica |
| `date_gmt` | date | The date the sample was taken in Greenwhich Mean Time. |
| `date_local` | date | The date the sample was taken in Local Standard Time. This represents only the date, the time is in a separate field. This time reflects the beginning of the sample duration. That is, if the time is 2:00 and the duration is 1-hour, then sampling happened from 2:00 - 3:00. |
| `date_of_last_change` | date | This represents the date the most relevant underlying data in AQS was last changed. That is, for annual summary data, it is the date these values were last affected by a change in raw data. If the AQCR code on the annual summary view changed, the date of last change would not be updated. |
| `datum` | string | The Datum associated with the Latitude and Longitude measures. The Datum represents the physical model of the earth used when determining latitude and longitude. AQS computes a "standard" location representation for all site location/coordinates so that data from AQS can be more easily used for mapping and geospatial analysis. This is accomplished using a geodatabase lookup to convert the user-provided coordinates into Latitude and Longitude with the standard horizontal datum of WGS84. (i.e. Thi |
| `detection_limit` | number | The minimum sample concentration detectable for the monitor and method. Each method has a federal MDL assigned to it by the EPA. If the analyzing agency has determined and reported their own MDL, this will be listed rather than the federal MDL. |
| `latitude` | number | The angular distance north or south of the equator measured in decimal degrees. North is positive. AQS converts reported coordinates (latitude and longitude) to the same datum so that sites can be more easily used for mapping and geospatial analysis. The standard datum is WGS84 and this is the latitude in the WGS84 datum. |
| `longitude` | number | The angular distance east or west of the prime meridian measured in decimal degrees. East is positive, West is negative. AQS converts reported coordinates (latitude and longitude) to the same datum so that sites can be more easily used for mapping and geospatial analysis. The standard datum is WGS84 and this is the longitude in the WGS84 datum. |
| `method` | string | A short description of the processes, equipment, and protocols used in gathering and measuring the sample. This field is a concatenation of the method of collection and the method of analysis. |
| `method_code` | string | A three-digit code representing the measurement method. A method code is only unique within a parameter (that is, method 132 for ozone is not the same as method 123 for benzene). The encoding contains both the sample collection and sample analysis descriptions. |
| `method_type` | string | An indication of whether the method used to collect the data is a federal reference method (FRM), equivalent to a federal reference method, an approved regional method, or none of the above (non-federal reference method). |
| `parameter` | string | The name or description assigned in AQS to the parameter measured by the monitor. Parameters may be pollutants or non-pollutants (e.g., wind speed). |
| `parameter_code` | string | The AQS code corresponding to the parameter measured by the monitor. |
| `poc` | number | This is the "Parameter Occurrence Code" used to distinguish different instruments that measure the same parameter at the same site. There is no meaning to the POC (e.g. POC 1 does not indicate the primary monitor). For example, the first monitor established to measure carbon monoxide (CO) at a site could have a POC of 1. If an additional monitor were established at the same site to measure CO, that monitor could have a POC of 2. However, if a new instrument were installed to replace the original |
| `qualifiers` | string | Sample values may have qualifiers that indicate why they are missing or that they are out of the ordinary. Types of qualifiers are: null data, exceptional event, natural events, and quality assurance. All Qualifiers are described in this field. |
| `sample_duration` | string | The length of time that air passes through the monitoring device before it is analyzed (measured). So, it represents an averaging period in the atmosphere (for example, a 24-hour sample duration draws ambient air over a collection filter for 24 straight hours). For continuous monitors, it can represent an averaging time of many samples (for example, a 1-hour value may be the average of four one-minute samples collected during each quarter of the hour). There are two types of sample durations. Fi |
| `sample_frequency` | string | The frequency at which sample observations are made. Specified as the amount of time that elapses between the beginning of subsequent observations. Usually, this indicates how often 24-hour samples are taken, e.g., daily, every third day, stratified random, etc. If this value is null, it implies continuous samples reported hourly. |
| `sample_measurement` | string | The measured value in the standard units of measure for the parameter. This value is calculated from the value reported to AQS using the following steps: * The units are converted from the reported units or measure to the AQS standard units of measure * The rounding and truncation rules for the parameter-method combination are applied. For example: |
| `site_number` | string | The 4-digit number used to uniquely identify the air monitoring site within a county or tribal land. The values are always numeric, but are treated as a string and padded with leading zeroes so they must always have 4 digits. There is no requirement that Site Numbers be assigned continuously or in any particular order. Regional or local organizations are thus free to allocate Site Numbers in any way they choose, as long as there is no duplication within a county or tribal area. Be aware that a t |
| `state` | string | The name of the state where the monitoring site is located. |
| `state_code` | string | The FIPS code of the state in which the monitor resides. AQS uses 2-digit or character codes that identifies one of the 50 states, U. S. territories, or Washington, DC. For border sites, the code '80' is used for Mexico and 'CC' is used for Canada. When submitting transactions, a user may opt to use the code 'TT' to indicate that this data is for a Native American Tribe, and that the next field on the transaction identifies a tribal area using the Bureau of Indian Affairs tribal code. Data in th |
| `time_gmt` | string | The time of day that sampling began on a 24-hour clock in Greenwich Mean Time. |
| `time_local` | string | The time of day that sampling began on a 24-hour clock in Local Standard Time. |
| `uncertainty` | number | The total measurement uncertainty associated with a reported measurement as indicated by the reporting agency. This includes method uncertainty, both the analytical and the volume uncertainty. No blank corrections are assumed (other than laboratory baseline corrections which are an integral part of each analysis). Uncertainty should be reported in the same units of measure as the Sample Value. |
| `units_of_measure` | string | The unit of measure for all statistics on the same row. Every parameter has a standard unit of measure. Submitters are allowed to report data in any unit and EPA converts to a standard unit so that we may use the data in calculations. |

## Native endpoint

Through the native Environmental Protection Agency API, this operation is `GET /sampleData/byBox` (base URL `https://aqs.epa.gov/data/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sample-data-by-box.md) for the provider-specific parameters and requirements.

