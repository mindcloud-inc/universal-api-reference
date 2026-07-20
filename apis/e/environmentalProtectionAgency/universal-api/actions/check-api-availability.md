# Environmental Protection Agency: Check API Availability

Retrieves API availability status from EPA AQS.

```
GET https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/check-api-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Environmental Protection Agency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/check-api-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/check-api-availability?${params}`, {
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
      "request_time": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request_time` | date | Server timestamp for the request. |
| `status` | string | EPA API availability status from the response header. |
| `url` | string | URL processed by EPA. |

## Native endpoint

Through the native Environmental Protection Agency API, this operation is `GET /metaData/isAvailable` (base URL `https://aqs.epa.gov/data/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-api-availability.md) for the provider-specific parameters and requirements.

