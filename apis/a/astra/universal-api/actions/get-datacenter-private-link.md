# Astra: Get Datacenter Private Link

Retrieves private link details for an Astra datacenter.

```
GET https://connect.mindcloud.co/v1/universal/astra/latest/actions/get-datacenter-private-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Astra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/astra/latest/actions/get-datacenter-private-link?connectionId=$CONNECTION_ID&databaseId=string&datacenterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "datacenterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/astra/latest/actions/get-datacenter-private-link?${params}`, {
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
| `databaseId` | string | yes | The Astra database ID. |
| `datacenterId` | string | yes | The Astra datacenter ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedPrincipals": [
        "string"
      ],
      "datacenterID": "string",
      "endpoints": [
        {}
      ],
      "serviceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedPrincipals` | array<string> | Allowed principals for the private link. |
| `datacenterID` | string | The datacenter ID. |
| `endpoints` | array<object> | Registered private-link endpoints. |
| `serviceName` | string | The cloud private-link service name. |

## Native endpoint

Through the native Astra API, this operation is `GET /v2/organizations/clusters/:databaseId/datacenters/:datacenterId/private-link` (base URL `https://api.astra.datastax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-datacenter-private-link.md) for the provider-specific parameters and requirements.

