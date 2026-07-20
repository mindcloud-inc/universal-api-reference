# Formitize: Get Job History

Retrieves a job's history from Formitize.

```
GET https://connect.mindcloud.co/v1/universal/formitize/latest/actions/get-job-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formitize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/get-job-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formitize/latest/actions/get-job-history?${params}`, {
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
| `id` | string | no | Formitize job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "lat": "string",
      "lng": "string",
      "startDate": "string",
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string |  |
| `lat` | string |  |
| `lng` | string |  |
| `startDate` | string |  |
| `text` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Formitize API, this operation is `GET /job/:id/history` (base URL `https://service.formitize.com/api/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-history.md) for the provider-specific parameters and requirements.

