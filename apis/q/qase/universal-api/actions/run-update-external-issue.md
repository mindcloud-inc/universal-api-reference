# Qase: Update external issues for runs

Updates external issue links for test runs in Qase.

```
PUT https://connect.mindcloud.co/v1/universal/qase/latest/actions/run-update-external-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qase/latest/actions/run-update-external-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "string",
  "type": "string",
  "links[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qase/latest/actions/run-update-external-issue', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "string",
    "type": "string",
    "links[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | Code of project, where to search entities. |
| `type` | string | yes | Required request field type. |
| `links[]` | array<object> | yes | Array of external issue links. Each test run (run_id) can have only one external issue link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Qase API, this operation is `POST /run/:code/external-issue` (base URL `https://api.qase.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-update-external-issue.md) for the provider-specific parameters and requirements.

