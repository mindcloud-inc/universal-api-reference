# USA.gov: Download English Site Top Downloads

Downloads yesterday's English site top downloads from USA.gov.

```
GET https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-top-downloads-yesterday-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USA.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-top-downloads-yesterday-csv?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-top-downloads-yesterday-csv?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw CSV response content. |

## Native endpoint

Through the native USA.gov API, this operation is `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/top-downloads-yesterday.csv` (base URL `https://s3-us-gov-west-1.amazonaws.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usagov-top-downloads-yesterday-csv.md) for the provider-specific parameters and requirements.

