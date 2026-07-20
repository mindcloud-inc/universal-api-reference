# Hy.page: Enroll in Sequence



```
POST https://connect.mindcloud.co/v1/universal/hypage/latest/actions/enroll-in-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/enroll-in-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "sequenceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hypage/latest/actions/enroll-in-sequence', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "sequenceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Existing person's email address. |
| `sequenceId` | string | yes | Email sequence ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enrolled": true,
      "peopleId": "string",
      "sequenceId": "string",
      "subscriptionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enrolled` | boolean |  |
| `peopleId` | string |  |
| `sequenceId` | string |  |
| `subscriptionId` | string |  |

## Native endpoint

Through the native Hy.page API, this operation is `POST /hyax-api/v1/sequences/enroll` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enroll-in-sequence.md) for the provider-specific parameters and requirements.

