# Sisense: Build Extract Datamodel

Starts an extract datamodel build in Sisense.

```
POST https://connect.mindcloud.co/v1/universal/sisense/latest/actions/build-extract-datamodel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/build-extract-datamodel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datamodelId": "string",
  "buildType": "full"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sisense/latest/actions/build-extract-datamodel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datamodelId": "string",
    "buildType": "full"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datamodelId` | string | yes | Datamodel OID to build. |
| `buildType` | string | yes | Build type: full, by_table, or schema_changes. Default: `full`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schemaOrigin` | string | no | Schema origin: latest or running. Default: `latest`. |
| `rowLimit` | number | no | Optional sample row limit. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `POST /api/v2/builds` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/build-extract-datamodel.md) for the provider-specific parameters and requirements.

