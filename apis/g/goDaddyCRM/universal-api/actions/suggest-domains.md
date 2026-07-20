# GoDaddy CRM: Suggest Domains

Suggests domains with the GoDaddy API.

```
GET https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/suggest-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/suggest-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/suggest-domains?${params}`, {
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
| `query` | string | no | Domain name or keywords for which alternative domains will be suggested. |
| `limit` | number | no | Maximum number of suggestions to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `country` | string | no | Two-letter ISO country code used as a target region hint. |
| `city` | string | no | City name used as a target region hint. |
| `sources[]` | array<string> | no | Suggestion sources to query. |
| `tlds[]` | array<string> | no | Top-level domains to include in suggestions. |
| `lengthMax` | number | no | Maximum length of the second-level domain. |
| `lengthMin` | number | no | Minimum length of the second-level domain. |
| `waitMs` | number | no | Maximum amount of time, in milliseconds, to wait for responses. Default: `1000`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `GET /v1/domains/suggest` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/suggest-domains.md) for the provider-specific parameters and requirements.

