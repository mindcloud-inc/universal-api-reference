# Leadboxer: Retrieve Lead Details

Retrieves lead details from Leadboxer.

```
GET https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/retrieve-lead-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadboxer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/retrieve-lead-details?connectionId=$CONNECTION_ID&leadId=string&email=ava%40example.com&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadId": "string",
  "email": "ava@example.com",
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/retrieve-lead-details?${params}`, {
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
| `leadId` | string | yes |  |
| `email` | string | yes |  |
| `site` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadboxer API returns.

## Native endpoint

Through the native Leadboxer API, this operation is `GET /v1/leads/{{leadId}}` (base URL `https://data.leadboxer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-lead-details.md) for the provider-specific parameters and requirements.

