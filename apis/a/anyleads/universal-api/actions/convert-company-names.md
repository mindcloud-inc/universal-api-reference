# Anyleads: Convert Company Names

Retrieves domain data for a company name from Anyleads.

```
GET https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/convert-company-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anyleads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/convert-company-names?connectionId=$CONNECTION_ID&companyName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/convert-company-names?${params}`, {
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
| `companyName` | string | yes | Company name to convert into a domain or normalized company data. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anyleads API returns.

## Native endpoint

Through the native Anyleads API, this operation is `POST /api-product/incoming-webhook/convert-company-names` (base URL `https://myapiconnect.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-company-names.md) for the provider-specific parameters and requirements.

