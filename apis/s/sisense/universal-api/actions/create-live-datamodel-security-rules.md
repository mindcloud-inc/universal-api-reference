# Sisense: Create Live Datamodel Security Rules

Creates live datamodel security rules in Sisense.

```
POST https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-live-datamodel-security-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-live-datamodel-security-rules" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "fullname": "Ava Chen",
  "table": "string",
  "column": "string",
  "datatype": "text",
  "allMembers": "true",
  "shares[0].partyId": "string",
  "shares[0].type": "user"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sisense/latest/actions/create-live-datamodel-security-rules', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "fullname": "Ava Chen",
    "table": "string",
    "column": "string",
    "datatype": "text",
    "allMembers": "true",
    "shares[0].partyId": "string",
    "shares[0].type": "user"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes |  |
| `fullname` | string | yes |  |
| `table` | string | yes |  |
| `column` | string | yes |  |
| `datatype` | string | yes | Default: `text`. |
| `allMembers` | boolean | yes | Default: `true`. |
| `shares[0].partyId` | string | yes |  |
| `shares[0].type` | string | yes | Default: `user`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sisense API returns.

## Native endpoint

Through the native Sisense API, this operation is `POST /api/v1/elasticubes/live/:title/datasecurity` (base URL `https://signup-126940n0.sisense.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-live-datamodel-security-rules.md) for the provider-specific parameters and requirements.

