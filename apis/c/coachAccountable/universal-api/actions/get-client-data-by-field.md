# CoachAccountable: Get Client Data By Field

Retrieves client data by field from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/get-client-data-by-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/get-client-data-by-field?connectionId=$CONNECTION_ID&fieldname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fieldname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/get-client-data-by-field?${params}`, {
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
| `fieldname` | string | yes | The name of the field to be fetched, either input name within a Form-based Worksheet, Metric name, or fedBy input name for a Metric. |
| `clientId` | number | no | The ID of the client for whom data is to be returned, if desired only for a single, specific client. |
| `dateFrom` | date | no | Set to restrict data returned to those dated at or after the provided value. |
| `dateTo` | date | no | Set to restrict data returned to those dated at or before the provided value. |
| `includeInactive` | boolean | no | Include data for Clients who are inactive. Default: `false`. |
| `dateBucket` | list | no | Group data dates to into weeks or months for a more coherent spreadsheet. Useful when, for example, clients all report on a weekly basis yet might do it on any day of the week. One of: `D`, `M`, `W`. Default: `W`. |
| `whatData` | list | no | Data points often have a sensible textual and numeric value. Set this to get one, the other, or both. One of: `B`, `N`, `T`. Default: `N`. |
| `structure` | list | no | How should the returned data be structured in the CSV? Date Grid means each row is a client, and columns are dates of the data. Data Point Listing returns rows that are each a single data point: ClientID, client name, date, and value. One of: `D`, `L`. Default: `D`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client-data-by-field.md) for the provider-specific parameters and requirements.

