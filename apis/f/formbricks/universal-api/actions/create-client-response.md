# Formbricks: Create Client Response

Creates a new client response in Formbricks.

```
POST https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/create-client-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formbricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/create-client-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "environmentId": "string",
  "surveyId": "string",
  "finished": true,
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/create-client-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "environmentId": "string",
    "surveyId": "string",
    "finished": true,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `environmentId` | string | yes | The environment ID that owns the survey. |
| `surveyId` | string | yes | The survey ID to submit the response to. |
| `finished` | boolean | yes | Whether the response is finished. |
| `data` | object | yes | Submitted response payload keyed by question IDs. |

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
| `data` | object | Created client response metadata. |
| `data.id` | string | Created response ID. |
| `data.quotaFull` | boolean | Whether the survey quota is full after creation. |

## Native endpoint

Through the native Formbricks API, this operation is `POST /client/:environmentId/responses` (base URL `https://app.formbricks.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client-response.md) for the provider-specific parameters and requirements.

