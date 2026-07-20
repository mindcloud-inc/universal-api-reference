# Formbricks: Update Client Response

Updates an existing client response in Formbricks.

```
PUT https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/update-client-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formbricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/update-client-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "environmentId": "string",
  "responseId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/update-client-response', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "environmentId": "string",
    "responseId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `environmentId` | string | yes | The environment ID that owns the survey response. |
| `responseId` | string | yes | The response ID to update. |
| `finished` | boolean | no | Whether the response is finished. |
| `data` | object | no | Updated response payload keyed by question IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": "string",
        "quotaFull": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Updated client response metadata. |
| `data.id` | string | Updated response ID. |
| `data.quotaFull` | boolean | Whether the survey quota is full after the update. |

## Native endpoint

Through the native Formbricks API, this operation is `PUT /client/:environmentId/responses/:responseId` (base URL `https://app.formbricks.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client-response.md) for the provider-specific parameters and requirements.

