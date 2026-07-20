# ClickHouse: Get Private Endpoint Configuration



```
GET https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-private-endpoint-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-private-endpoint-configuration?connectionId=$CONNECTION_ID&organizationId=string&serviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string",
  "serviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-private-endpoint-configuration?${params}`, {
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
| `organizationId` | string | yes | ID of the organization that owns the service. |
| `serviceId` | string | yes | ID of the requested service. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endpointServiceId": "string",
      "privateDnsHostname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpointServiceId` | string | Unique identifier of the private endpoint service. |
| `privateDnsHostname` | string | Private DNS hostname for the configured private endpoint. |

## Native endpoint

Through the native ClickHouse API, this operation is `GET /v1/organizations/[:organizationId]/services/[:serviceId]/privateEndpointConfig` (base URL `https://api.clickhouse.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-private-endpoint-configuration.md) for the provider-specific parameters and requirements.

