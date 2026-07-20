# Survicate: Get Personal Data Counters

Retrieves personal data counts by email from Survicate.

```
GET https://connect.mindcloud.co/v1/universal/survicate/latest/actions/get-personal-data-counters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survicate/latest/actions/get-personal-data-counters?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survicate/latest/actions/get-personal-data-counters?${params}`, {
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
| `email` | string | yes | The email address to search for across all data sources. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "insightsHub": {
        "authorAttributes": 1,
        "authors": 1,
        "notes": 1,
        "notesAttributes": 1,
        "total": 1
      },
      "respondents": 1,
      "responses": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `insightsHub.authorAttributes` | number | Number of Insights Hub author attribute records. |
| `insightsHub.authors` | number | Number of Insights Hub author records. |
| `insightsHub.notes` | number | Number of Insights Hub note records. |
| `insightsHub.notesAttributes` | number | Number of Insights Hub note attribute records. |
| `insightsHub.total` | number | Total number of Insights Hub records. |
| `respondents` | number | Total number of respondent records associated with the email address. |
| `responses` | number | Total number of survey responses associated with the email address. |

## Native endpoint

Through the native Survicate API, this operation is `GET /personal-data` (base URL `https://data-api.survicate.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-personal-data-counters.md) for the provider-specific parameters and requirements.

