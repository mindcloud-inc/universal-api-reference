# Harness: Create Connector

Creates a new connector in Harness.

```
POST https://connect.mindcloud.co/v1/universal/harness/latest/actions/create-connector
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harness `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harness/latest/actions/create-connector" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "connector.identifier": "string",
  "connector.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harness/latest/actions/create-connector', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "connector.identifier": "string",
    "connector.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `connector.description` | string | no | Connector description. |
| `connector.identifier` | string | yes | Connector identifier. |
| `connector.name` | string | yes | Connector display name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connector": {},
      "createdAt": 1,
      "lastModifiedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connector` | object | Created connector payload. |
| `createdAt` | number | Connector creation timestamp in milliseconds. |
| `lastModifiedAt` | number | Connector update timestamp in milliseconds. |

## Native endpoint

Through the native Harness API, this operation is `POST /ng/api/connectors` (base URL `https://app.harness.io/gateway`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-connector.md) for the provider-specific parameters and requirements.

