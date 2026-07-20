# Dromo: Create SFTP Connector

Creates a new SFTP connector in Dromo.

```
POST https://connect.mindcloud.co/v1/universal/dromo/latest/actions/create-sftp-connector
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dromo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dromo/latest/actions/create-sftp-connector" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "credentials": "string",
  "schema": "string",
  "schedule": {},
  "directory": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dromo/latest/actions/create-sftp-connector', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `credentials` | string | yes | Request body field credentials. |
| `schema` | string | yes | Request body field schema. |
| `schedule` | object | yes | Request body field schedule. |
| `directory` | string | yes | Request body field directory. |
| `file_regex` | string | no | Request body field file_regex. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dromo API returns.

## Native endpoint

Through the native Dromo API, this operation is `POST /headless/sftp/connectors/` (base URL `https://app.dromo.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sftp-connector.md) for the provider-specific parameters and requirements.

