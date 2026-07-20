# PredictLeads: List Companies

Retrieves companies from the PredictLeads API.

```
GET https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PredictLeads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0&location=United%20States&sizes=11-50" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "location": "United States",
  "sizes": "11-50"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-companies?${params}`, {
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
| `location` | string | yes | The response will include only companies located in the given country name or state name/abbreviation. Example: `United States`. |
| `sizes` | string | yes | Company size filter. Official docs describe one or more valid sizes; runtime succeeded with a scalar query value such as `11-50`. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. Example: `11-50`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PredictLeads API returns.

## Native endpoint

Through the native PredictLeads API, this operation is `GET /discover/companies` (base URL `https://predictleads.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

