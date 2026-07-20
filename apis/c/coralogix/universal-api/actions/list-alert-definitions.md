# Coralogix: List Alert Definitions



```
GET https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-alert-definitions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coralogix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-alert-definitions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-alert-definitions?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `queryFilter` | string | no | Optional query_filter query parameter supported by the Coralogix OpenAPI endpoint. |
| `pagination` | string | no | Optional pagination query parameter supported by the Coralogix OpenAPI endpoint. |
| `orderBys` | string | no | Optional order_bys query parameter supported by the Coralogix OpenAPI endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alertDefs": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alertDefs` | array<object> | alertDefs returned by Coralogix. |
| `pagination` | object | pagination returned by Coralogix. |

## Native endpoint

Through the native Coralogix API, this operation is `GET /alerts/alerts-general/v3` (base URL `https://api.eu2.coralogix.com/mgmt/openapi/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alert-definitions.md) for the provider-specific parameters and requirements.

