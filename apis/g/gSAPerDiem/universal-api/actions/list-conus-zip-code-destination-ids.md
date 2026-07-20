# GSA Per Diem: List CONUS ZIP Code Destination IDs

Retrieves CONUS ZIP code destination IDs from GSA Per Diem.

```
GET https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-conus-zip-code-destination-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GSA Per Diem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-conus-zip-code-destination-ids?connectionId=$CONNECTION_ID&year=2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSAPerDiem/latest/actions/list-conus-zip-code-destination-ids?${params}`, {
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
| `year` | string | yes | Fiscal year of travel. GSA documents up to three years available. Example: `2026`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "DID": "string",
      "ST": "string",
      "Zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DID` | string | Destination ID for the ZIP/state pair. |
| `ST` | string | State abbreviation associated with the destination ID. |
| `Zip` | string | ZIP code associated with the destination ID. |

## Native endpoint

Through the native GSA Per Diem API, this operation is `GET /rates/conus/zipcodes/:year` (base URL `https://api.gsa.gov/travel/perdiem/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conus-zip-code-destination-ids.md) for the provider-specific parameters and requirements.

