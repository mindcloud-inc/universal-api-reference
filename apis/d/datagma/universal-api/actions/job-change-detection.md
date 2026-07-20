# Datagma: Job Change Detection

Retrieves job change details from Datagma.

```
GET https://connect.mindcloud.co/v1/universal/datagma/latest/actions/job-change-detection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datagma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datagma/latest/actions/job-change-detection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datagma/latest/actions/job-change-detection?${params}`, {
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
| `company` | string | no | Target company name. |
| `debug` | string | no | Set false to allow broader scoring results. |
| `email` | string | no | Email address used as a high-certainty input for job change detection. |
| `full_name` | string | no | Target person's full name. |
| `linked_in_url` | string | no | LinkedIn profile URL used for higher-certainty job change detection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyScore": 1,
      "creditBurn": "string",
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyScore` | number |  |
| `creditBurn` | string |  |
| `data` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Datagma API, this operation is `GET /v4/update` (base URL `https://gateway.datagma.net/api/ingress`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/job-change-detection.md) for the provider-specific parameters and requirements.

