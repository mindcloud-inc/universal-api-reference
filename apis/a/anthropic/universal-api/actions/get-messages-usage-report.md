# Anthropic: Get Messages Usage Report

Retrieves the Anthropic messages usage report.

```
GET https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/get-messages-usage-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/get-messages-usage-report?connectionId=$CONNECTION_ID&startingAt=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startingAt": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/get-messages-usage-report?${params}`, {
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
| `startingAt` | string | yes | Start timestamp (inclusive) for the report window. |
| `endingAt` | string | no | End timestamp (exclusive) for the report window. |
| `bucketWidth` | string | no | Aggregation bucket width. |
| `groupBy` | list<string> | no | Dimensions used to group usage metrics. |
| `workspaceIds` | list<string> | no | Filter by workspace IDs. |
| `apiKeyIds` | list<string> | no | Filter by API key IDs. |
| `model` | string | no | Filter by model name. |
| `limit` | number | no | Number of rows per page. |
| `page` | number | no | Page number for pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "hasMore": true,
      "nextPage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Usage report rows. |
| `hasMore` | boolean | Whether more report pages are available. |
| `nextPage` | string | Opaque token for the next page. |

## Native endpoint

Through the native Anthropic API, this operation is `GET /v1/organizations/usage_report/messages` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-messages-usage-report.md) for the provider-specific parameters and requirements.

