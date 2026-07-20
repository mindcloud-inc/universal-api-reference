# Coresignal: Collect Multi-source Job By ID

Collects a multi-source job from Coresignal by ID.

```
GET https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-multi-source-job-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-multi-source-job-by-id?connectionId=$CONNECTION_ID&jobId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-multi-source-job-by-id?${params}`, {
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
| `jobId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_domain": "string",
      "company_name": "Ava Chen",
      "country": "string",
      "employment_type": "string",
      "id": 1,
      "location": "string",
      "seniority": "string",
      "title": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_domain` | string |  |
| `company_name` | string |  |
| `country` | string |  |
| `employment_type` | string |  |
| `id` | number |  |
| `location` | string |  |
| `seniority` | string |  |
| `title` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Coresignal API, this operation is `GET /job_multi_source/collect/:jobId` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/collect-multi-source-job-by-id.md) for the provider-specific parameters and requirements.

