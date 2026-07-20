# Astra: List Database Datacenters

Retrieves datacenters for an Astra database.

```
GET https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-database-datacenters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Astra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-database-datacenters?connectionId=$CONNECTION_ID&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/astra/latest/actions/list-database-datacenters?${params}`, {
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
| `all` | boolean | no | Include terminated datacenters when true. |
| `databaseId` | string | yes | The Astra database ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capacityUnits": 1,
      "cloudProvider": "string",
      "cqlshUrl": "https://example.com",
      "dataEndpointUrl": "https://example.com",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "graphqlUrl": "https://example.com",
      "id": "string",
      "isPrimary": true,
      "name": "Ava Chen",
      "region": "string",
      "regionClassification": "string",
      "regionZone": "string",
      "secureBundleUrl": "https://example.com",
      "status": "string",
      "tier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacityUnits` | number | Provisioned capacity units. |
| `cloudProvider` | string | The cloud provider. |
| `cqlshUrl` | string | The CQL shell URL. |
| `dataEndpointUrl` | string | The REST data endpoint URL. |
| `dateCreated` | date | When the datacenter was created. |
| `graphqlUrl` | string | The GraphQL endpoint URL. |
| `id` | string | The datacenter ID. |
| `isPrimary` | boolean | Whether this is the primary datacenter. |
| `name` | string | The datacenter name. |
| `region` | string | The cloud region. |
| `regionClassification` | string | The region classification. |
| `regionZone` | string | The region zone bucket. |
| `secureBundleUrl` | string | The secure bundle download URL when available. |
| `status` | string | The datacenter status. |
| `tier` | string | The Astra tier for the datacenter. |

## Native endpoint

Through the native Astra API, this operation is `GET /v2/databases/:databaseId/datacenters` (base URL `https://api.astra.datastax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-database-datacenters.md) for the provider-specific parameters and requirements.

