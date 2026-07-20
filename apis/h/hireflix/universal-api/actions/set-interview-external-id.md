# Hireflix: Set Interview External ID

Updates an interview external ID in Hireflix.

```
PUT https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/set-interview-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/set-interview-external-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.id": "string",
  "variables.externalId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/set-interview-external-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.id": "string",
    "variables.externalId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.id` | string | yes | The Hireflix interview ID. |
| `variables.externalId` | string | yes | The external identifier to set on the interview. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalId": "string",
      "id": "string",
      "status": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalId` | string |  |
| `id` | string |  |
| `status` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-interview-external-id.md) for the provider-specific parameters and requirements.

