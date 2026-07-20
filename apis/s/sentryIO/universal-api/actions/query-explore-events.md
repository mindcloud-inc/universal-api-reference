# Sentry IO: Query Explore Events

Queries table-format explore events in Sentry IO.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/query-explore-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/query-explore-events?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org&dataset=0&field=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org",
  "dataset": "0",
  "field": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/query-explore-events?${params}`, {
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
| `organizationIdOrSlug` | string | yes | The Sentry organization ID or slug. Example: `my-org`. |
| `dataset` | list | yes | The Explore dataset to query, such as errors, transactions, spans, logs, or discover. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `field` | string | yes | A single Sentry Explore field, function, or equation to include in the table result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Explore event rows. |
| `meta` | object | Field metadata returned by Explore. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /organizations/:organization_id_or_slug/events/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-explore-events.md) for the provider-specific parameters and requirements.

