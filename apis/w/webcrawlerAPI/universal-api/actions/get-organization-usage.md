# Webcrawler API: Get Organization Usage

Retrieves organization usage statistics from Webcrawler API.

```
GET https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-organization-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webcrawler API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-organization-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-organization-usage?${params}`, {
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
| `from` | string | no | Start date in YYYY-MM-DD format. |
| `to` | string | no | End date in YYYY-MM-DD format. |
| `include_daily` | boolean | no | Include daily breakdown in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "costUsd": 1,
      "from": "string",
      "orgId": "string",
      "requests": 1,
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `costUsd` | number | Total usage cost in USD for the requested period. |
| `from` | string | Usage period start date. |
| `orgId` | string | Organization identifier. |
| `requests` | number | Total request count for the requested period. |
| `to` | string | Usage period end date. |

## Native endpoint

Through the native Webcrawler API API, this operation is `GET /v2/organization/usage` (base URL `https://api.webcrawlerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-usage.md) for the provider-specific parameters and requirements.

