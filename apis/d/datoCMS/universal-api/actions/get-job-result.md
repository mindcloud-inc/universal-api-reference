# DatoCMS: Get Job Result



```
GET https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-job-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-job-result?connectionId=$CONNECTION_ID&jobResultId=a8d0d179b809101255a2145f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobResultId": "a8d0d179b809101255a2145f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-job-result?${params}`, {
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
| `jobResultId` | string | yes | Example: `a8d0d179b809101255a2145f`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Job result payload and status details |
| `id` | string | Job result ID |
| `type` | string | Resource type |

## Native endpoint

Through the native DatoCMS API, this operation is `GET /job-results/:jobResultId` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-result.md) for the provider-specific parameters and requirements.

