# Memberstack: Create Data Record



```
POST https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/create-data-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memberstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/create-data-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableKey": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/create-data-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableKey": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableKey` | string | yes | Target data table key. |
| `data` | object | yes | Record payload object to create in the table. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "data": {},
      "id": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `data` | object |  |
| `id` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Memberstack API, this operation is `POST /v2/data-tables/:tableKey/records` (base URL `https://admin.memberstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-data-record.md) for the provider-specific parameters and requirements.

