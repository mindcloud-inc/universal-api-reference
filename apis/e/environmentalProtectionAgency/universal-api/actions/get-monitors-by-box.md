# Environmental Protection Agency: Get Monitors By Box

Retrieves monitors for a bounding box from EPA AQS.

```
GET https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-monitors-by-box
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Environmental Protection Agency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-monitors-by-box?connectionId=$CONNECTION_ID&bdate=20170101&edate=20171231&minlat=33.3&maxlat=33.6&minlon=-87.0&maxlon=-86.7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bdate": "20170101",
  "edate": "20171231",
  "minlat": "33.3",
  "maxlat": "33.6",
  "minlon": "-87.0",
  "maxlon": "-86.7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/get-monitors-by-box?${params}`, {
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
| `bdate` | string | yes | Begin date in YYYYMMDD format. Example: `20170101`. |
| `edate` | string | yes | End date in YYYYMMDD format. EPA requires this to be in the same year as the begin date except for monitors. Example: `20171231`. |
| `minlat` | number | yes | Southern latitude bound for a geographic box query. Example: `33.3`. |
| `maxlat` | number | yes | Northern latitude bound for a geographic box query. Example: `33.6`. |
| `minlon` | number | yes | Western longitude bound for a geographic box query. Use negative values in the western hemisphere. Example: `-87.0`. |
| `maxlon` | number | yes | Eastern longitude bound for a geographic box query. Use negative values in the western hemisphere. Example: `-86.7`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `param` | string | no | Optional AQS parameter code filter. Use up to five comma-separated 5-digit parameter codes. Accepts multiple values in one string, delimited by `,`. Example: `44201`. |
| `cbdate` | string | no | Optional begin date in YYYYMMDD format for filtering by date of last change. Example: `20180101`. |
| `cedate` | string | no | Optional end date in YYYYMMDD format for filtering by date of last change. Example: `20181231`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analyzing_agency": "string",
      "analyzing_agency_code": "string",
      "auditing_agency": "string",
      "auditing_agency_code": "string",
      "cbsa": "string",
      "cbsa_code": "string",
      "certifying_agency": "string",
      "certifying_agency_code": "string",
      "city": "string",
      "close_date": "2026-05-07T12:00:00.000Z",
      "collecting_agency": "string",
      "collecting_agency_code": "string",
      "concurred_exclusions": "string",
      "county": 1,
      "county_code": "string",
      "csa": "string",
      "csa_code": "string",
      "datum": "string",
      "dominant_source": "string",
      "last_method_begin_date": "2026-05-07T12:00:00.000Z",
      "last_method_code": "string",
      "last_method_description": "string",
      "lat_lon_accuracy": "string",
      "latitude": 1,
      "local_site_name": "Ava Chen",
      "longitude": 1,
      "measurement_scale": "string",
      "measurement_scale_def": "string",
      "monitor_type": "string",
      "monitoring_objective": "string",
      "naaqs_primary_monitor": "string",
      "networks": "string",
      "open_date": "2026-05-07T12:00:00.000Z",
      "parameter": "string",
      "parameter_code": "string",
      "poc": 1,
      "pqao": "string",
      "pqao_code": "string",
      "probe_height": "string",
      "probe_location": "string",
      "qa_primary_monitor": "string",
      "reporting_agency": "string",
      "reporting_agency_code": "string",
      "site_address": "string",
      "site_elevation": "string",
      "site_number": "string",
      "state": "string",
      "state_code": "string",
      "tribal_code": "string",
      "tribe": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analyzing_agency` | string | The name of the agency assigned as "Analyzing" for the monitor reporting data. |
| `analyzing_agency_code` | string | The code of the agency assigned as "Analyzing" for the monitor reporting data. |
| `auditing_agency` | string | The name of the agency assigned as "Auditing" for the monitor reporting data. |
| `auditing_agency_code` | string | The code of the agency assigned as "Auditing" for the monitor reporting data. |
| `cbsa` | string | The shortened name of the core based statistical area (metropolitan area) where the monitoring site is located. |
| `cbsa_code` | string | The code of the core based statistical area (metropolitan area) where the monitoring site is located. |
| `certifying_agency` | string | The name of the agency assigned as "Certifying" for the monitor reporting data. This is the organization who must attest to the completeness and accuracy of the data after all of the data for a calendar year is collected and reported. |
| `certifying_agency_code` | string | The code of the agency assigned as "Certifying" for the monitor reporting data. |
| `city` | string | The name of the city where the monitoring site is located. This represents the legal incorporated boundaries of cities and not urban areas. |
| `close_date` | date | The date on which the operating agency indicated that all activity associated with tihs monitor has ended. If this field is populated, all monitor subordinate records are automatically populated with the same close date. Removing this date will NOT automatically remove the close date from monitor subordinate records - that must be done manually. As distinct from "closed", AQS usually determines if a mointor is "operating" by looking at the date the last sampling period ended. If a monitor is clo |
| `collecting_agency` | string | The name of the agency assigned as "Collecting" for the monitor reporting data. |
| `collecting_agency_code` | string | The code of the agency assigned as "Collecting" for the monitor reporting data. |
| `concurred_exclusions` | string | If the operating agency has requested that data from this monitor be excluded from NAAQS calculations and the governing EPA regional office has agreed, the NAAQS standard(s) and the years of exclusion are listed. |
| `county` | number | The name of the county where the monitoring site is located. |
| `county_code` | string | A Federal Information Processing Standards (FIPS) code that identifies a county, parish, or independent city within a state. In certain cases other geo-political entities, such as tribe via the BIA tribal code, may be used. For border sites, it identifies the geo-political equivalent to U. S. states, such as Mexican states or Canadian provinces. When submitting transactions, a user may opt to use a Bureau of Indian Affairs tribal code in this fied (if the State Code was entered as 'TT' to indica |
| `csa` | string | The shortened name of the combined statistical area where the monitoring site is located. |
| `csa_code` | string | The code of the combined statistical area where the monitoring site is located. |
| `datum` | string | The Datum associated with the Latitude and Longitude measures. The Datum represents the physical model of the earth used when determining latitude and longitude. AQS computes a "standard" location representation for all site location/coordinates so that data from AQS can be more easily used for mapping and geospatial analysis. This is accomplished using a geodatabase lookup to convert the user-provided coordinates into Latitude and Longitude with the standard horizontal datum of WGS84. (i.e. Thi |
| `dominant_source` | string | The primary source of the pollutant being monitored, e.g., point, area, mobile. |
| `last_method_begin_date` | date | Many tables show the method currently used by a monitor. This field shows the date on which that method began being used for the monitor. |
| `last_method_code` | string | Many tables show the method currently used by a monitor. This field shows the AQS method code for that method. |
| `last_method_description` | string | Many tables show the method currently used by a monitor. This field shows the description of that method. The description is a concatenation of the sample Method of Collection and Method of Analysis. |
| `lat_lon_accuracy` | string | The accuracy of the latitude and longitude coordinates in meters. Only the least accurate measurement needs to be recorded, whether it is latitude or longitude. For Global Positioning System (GPS), the accuracy values vary. The type of GPS used along with operating conditions affect accuracy. The GPS receiver may provide accuracy values associated with specific coordinate readings. For map interpolation, the accuracy will depend on the scale of the map and the method of interpolation. For exampl |
| `latitude` | number | The angular distance north or south of the equator measured in decimal degrees. North is positive. AQS converts reported coordinates (latitude and longitude) to the same datum so that sites can be more easily used for mapping and geospatial analysis. The standard datum is WGS84 and this is the latitude in the WGS84 datum. |
| `local_site_name` | string | The identifier of the site in the onwning agency's (e.g., not US EPA) nomenclature. AQS makes no use of this field, but provides it on some output for the convenience of users. |
| `longitude` | number | The angular distance east or west of the prime meridian measured in decimal degrees. East is positive, West is negative. AQS converts reported coordinates (latitude and longitude) to the same datum so that sites can be more easily used for mapping and geospatial analysis. The standard datum is WGS84 and this is the longitude in the WGS84 datum. |
| `measurement_scale` | string | A denotation of the geographic scope of the air quality measurements made by the monitor. The implication is that the same measurement made elsewhere within the measurement scale would produce an equivalent result to that produced at the monitoring site. |
| `measurement_scale_def` | string | A numeric distance that reflects the Measurement Scale geographic scope. |
| `monitor_type` | string | An administrative or regulatory classification for the monitor. Fopr example a specification of the monitor's agency organizational level such as EPA, or SLAMS, or Industrial. |
| `monitoring_objective` | string | Identification of the reason for measuring air quality by the monitor. |
| `naaqs_primary_monitor` | string | An indication of whether this is the primary monitor for the pollutant at the site for standards compliance when more than one monitor is operating at the site. |
| `networks` | string | The name of the Network(s) the monitor is associated with. |
| `open_date` | date | The date on which a monitor commenced collecting data. |
| `parameter` | string | The name or description assigned in AQS to the parameter measured by the monitor. Parameters may be pollutants or non-pollutants (e.g., wind speed). |
| `parameter_code` | string | The AQS code corresponding to the parameter measured by the monitor. |
| `poc` | number | This is the "Parameter Occurrence Code" used to distinguish different instruments that measure the same parameter at the same site. There is no meaning to the POC (e.g. POC 1 does not indicate the primary monitor). For example, the first monitor established to measure carbon monoxide (CO) at a site could have a POC of 1. If an additional monitor were established at the same site to measure CO, that monitor could have a POC of 2. However, if a new instrument were installed to replace the original |
| `pqao` | string | The name of the agency assigned as Primary Quality Assurance Organization for the monitor reporting data. |
| `pqao_code` | string | The code representing the Primary Quality Assurance Organization for this monitor. |
| `probe_height` | string | The height of the monitor's sampling probe from the ground, in meters. |
| `probe_location` | string | A general location of the monitor's probe with respect to structures at the monitoring site. Valid values are: * GROUND LEVEL SUPPORT * POLE * SIDE OF BUILDING * TOP OF BUILDING * TOWER * OTHER |
| `qa_primary_monitor` | string | An indication of whether this is the primary monitor for the pollutant at the site when collocated monitors are used for quality assurance purposes. Enter a Y if this is the primary sampler or an N if this is a duplicate/non-primary monitor. |
| `reporting_agency` | string | The name of the agency assigned as "Reporting" data for the monitor reporting data. |
| `reporting_agency_code` | string | The code of the agency assigned as "Reporting" data for the monitor reporting data. |
| `site_address` | string | The street address giving an approximate location (building number and street; or other descriptor) of the site. |
| `site_elevation` | string | The elevation of the ground at the site in meters above mean sea level. |
| `site_number` | string | The 4-digit number used to uniquely identify the air monitoring site within a county or tribal land. The values are always numeric, but are treated as a string and padded with leading zeroes so they must always have 4 digits. There is no requirement that Site Numbers be assigned continuously or in any particular order. Regional or local organizations are thus free to allocate Site Numbers in any way they choose, as long as there is no duplication within a county or tribal area. Be aware that a t |
| `state` | string | The name of the state where the monitoring site is located. |
| `state_code` | string | The FIPS code of the state in which the monitor resides. AQS uses 2-digit or character codes that identifies one of the 50 states, U. S. territories, or Washington, DC. For border sites, the code '80' is used for Mexico and 'CC' is used for Canada. When submitting transactions, a user may opt to use the code 'TT' to indicate that this data is for a Native American Tribe, and that the next field on the transaction identifies a tribal area using the Bureau of Indian Affairs tribal code. Data in th |
| `tribal_code` | string | The BIA code representing the tribe on whose land the monitoring site resides. This is an optional way of displaying data. A tribe may (or may not) chose to enter their site's geographic location data using tribal code (rather than a state and county code). |
| `tribe` | string | The BIA name of the tribe with responsibility for operating the monitor, reporting data, etc. |

## Native endpoint

Through the native Environmental Protection Agency API, this operation is `GET /monitors/byBox` (base URL `https://aqs.epa.gov/data/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-monitors-by-box.md) for the provider-specific parameters and requirements.

