# Datadog: List SLOs

Retrieves service level objectives from Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-sl-os
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-sl-os?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-sl-os?${params}`, {
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
| `ids` | string | no | Comma-separated SLO IDs. |
| `query` | string | no | Filter SLOs by name. |
| `tagsQuery` | string | no | Filter SLOs by a tag query. |
| `metricsQuery` | string | no | Filter SLOs by numerator and denominator query. |
| `limit` | number | no | Maximum number of SLOs to return. |
| `offset` | number | no | Offset for SLO pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "error": "string",
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Service level objectives returned by the request. |
| `error` | string | Error returned by the API, if any. |
| `metadata` | object | Metadata for the SLO list response. |

## Native endpoint

Through the native Datadog API, this operation is `GET /api/v1/slo` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sl-os.md) for the provider-specific parameters and requirements.

