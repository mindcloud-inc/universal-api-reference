# Statsig: Patch Entity Property Source

Updates an entity property source in Statsig.

```
PUT https://connect.mindcloud.co/v1/universal/statsig/latest/actions/patch-entity-property-source-patch-console-v1-experiments-entity-property-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/patch-entity-property-source-patch-console-v1-experiments-entity-property-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/patch-entity-property-source-patch-console-v1-experiments-entity-property-name', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of entity property source |
| `description` | string | no | Request body field. |
| `tags` | list | no | Request body field. |
| `sql` | string | no | Request body field. |
| `timestampColumn` | string | no | Request body field. |
| `timestampAsDay` | boolean | no | Request body field. |
| `idTypeMapping` | list | no | Request body field. |
| `isReadOnly` | boolean | no | Request body field. |
| `team` | string | no | Request body field. |
| `teamID` | string | no | Request body field. |
| `dryRun` | boolean | no | Request body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `PATCH /console/v1/experiments/entity_property/{name}` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-entity-property-source-patch-console-v1-experiments-entity-property-name.md) for the provider-specific parameters and requirements.

