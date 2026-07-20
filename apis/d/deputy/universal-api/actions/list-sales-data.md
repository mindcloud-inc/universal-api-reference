# Deputy: List Sales Data

Retrieves raw sales metrics from Deputy.

```
GET https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-sales-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-sales-data?connectionId=$CONNECTION_ID&areas=string&end=1&start=1&types=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "areas": "string",
  "end": "1",
  "start": "1",
  "types": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-sales-data?${params}`, {
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
| `areas` | string | yes | Comma-separated Deputy area IDs. |
| `end` | number | yes | Unix timestamp for the end of the reporting window. |
| `start` | number | yes | Unix timestamp for the start of the reporting window. |
| `types` | string | yes | Comma-separated metric types, for example Sales or Transactions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "area": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "employee": 1,
      "id": "string",
      "location": 1,
      "modified": "2026-05-07T12:00:00.000Z",
      "reference": "string",
      "state": "string",
      "timestamp": 1,
      "type": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `area` | number |  |
| `created` | date |  |
| `employee` | number |  |
| `id` | string |  |
| `location` | number |  |
| `modified` | date |  |
| `reference` | string |  |
| `state` | string |  |
| `timestamp` | number |  |
| `type` | string |  |
| `value` | number |  |

## Native endpoint

Through the native Deputy API, this operation is `GET /api/v2/metrics/raw` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales-data.md) for the provider-specific parameters and requirements.

