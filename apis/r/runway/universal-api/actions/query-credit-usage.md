# Runway: Query Credit Usage

Retrieves organization credit usage from Runway.

```
GET https://connect.mindcloud.co/v1/universal/runway/latest/actions/query-credit-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runway/latest/actions/query-credit-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runway/latest/actions/query-credit-usage?${params}`, {
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
| `beforeDate` | string | no | UTC exclusive end date in YYYY-MM-DD format. Defaults to tomorrow if omitted. |
| `startDate` | string | no | UTC start date in YYYY-MM-DD format for usage aggregation. Defaults to 30 days ago if omitted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "models": [
        "string"
      ],
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `models` | array<string> |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Runway API, this operation is `POST /v1/organization/usage` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-credit-usage.md) for the provider-specific parameters and requirements.

