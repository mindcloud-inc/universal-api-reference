# Veracity Learning: Create Statements

Creates one or more statements in Veracity Learning.

```
POST https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/create-statements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/create-statements" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "statements[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/create-statements', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "statements[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statements[]` | array<object> | yes | Array of xAPI Statement objects to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "statementId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `statementId` | string | Statement identifier returned by the LRS after creating a statement. |

## Native endpoint

Through the native Veracity Learning API, this operation is `POST /statements` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-statements.md) for the provider-specific parameters and requirements.

