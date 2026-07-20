# Dromo: Update SFTP Connector

Updates an existing SFTP connector in Dromo.

```
PUT https://connect.mindcloud.co/v1/universal/dromo/latest/actions/update-sftp-connector
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dromo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dromo/latest/actions/update-sftp-connector" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "credentials": "string",
  "schema": "string",
  "schedule": {},
  "directory": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dromo/latest/actions/update-sftp-connector', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "credentials": "string",
    "schema": "string",
    "schedule": {},
    "directory": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Path parameter id. |
| `credentials` | string | yes | Request body field credentials. |
| `schema` | string | yes | Request body field schema. |
| `schedule` | object | yes | Request body field schedule. |
| `directory` | string | yes | Request body field directory. |
| `file_regex` | string | no | Request body field file_regex. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dromo API returns.

## Native endpoint

Through the native Dromo API, this operation is `PUT /headless/sftp/connectors/:id/` (base URL `https://app.dromo.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sftp-connector.md) for the provider-specific parameters and requirements.

