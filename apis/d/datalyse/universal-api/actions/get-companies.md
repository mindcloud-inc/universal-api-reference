# Datalyse: Get Companies

Retrieves a list of companies from Datalyse.

```
GET https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/get-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datalyse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/get-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/get-companies?${params}`, {
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
| `agentId` | string | no | Show only results for this agent ID (optional) |
| `dateFrom` | string | no | Start date for filtering results (optional, format: YYYY-MM-DD) |
| `dateTo` | string | no | End date for filtering results (optional, format: YYYY-MM-DD) |
| `page` | string | no | Page number Default: `1`. |
| `resultsPerPage` | string | no | Maximum number of results to display Default: `20`. |
| `searchValue` | string | no | Text to search for (optional) |
| `statusId` | string | no | Show only results with this status (optional) |
| `timezone` | string | no | Timezone for date filtering (optional, example: Europe/Madrid) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | API response status |

## Native endpoint

Through the native Datalyse API, this operation is `POST /api/1.0/companies/get.json` (base URL `https://api.datalyse.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-companies.md) for the provider-specific parameters and requirements.

