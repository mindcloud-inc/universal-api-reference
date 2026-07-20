# Certs 365: Get Status Graph Data

Retrieves monthly status graph data from Certs 365.

```
GET https://connect.mindcloud.co/v1/universal/certs365/latest/actions/get-status-graph-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certs 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/get-status-graph-data?connectionId=$CONNECTION_ID&month=1&year=1&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "month": "1",
  "year": "1",
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certs365/latest/actions/get-status-graph-data?${params}`, {
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
| `month` | number | yes | Month to retrieve status graph data for. |
| `year` | number | yes | Year to retrieve status graph data for. |
| `email` | string | yes | Issuer email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": 1,
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | number |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Certs 365 API, this operation is `GET /api/get-status-graph-data/{month}/{year}/{email}` (base URL `https://api1.certs365.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-status-graph-data.md) for the provider-specific parameters and requirements.

