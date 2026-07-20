# OneSuite: Convert Opportunity to Client

Converts an opportunity to a client in OneSuite.

```
PUT https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/convert-opportunity-to-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/convert-opportunity-to-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "opportunityId": "cmo7h1vjm02stbo05mhgr2rmy"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/convert-opportunity-to-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "opportunityId": "cmo7h1vjm02stbo05mhgr2rmy"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `opportunityId` | string | yes | Opportunity ID from the convert-opportunity docs. Example: `cmo7h1vjm02stbo05mhgr2rmy`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | no | Optional company ID if different from the opportunity's connected company. Example: `cmo7gzxna02smbo056u59sb9y`. |
| `message` | string | no | Optional invitation message for invited people. Example: `Welcome to our client portal!`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneSuite API returns.

## Native endpoint

Through the native OneSuite API, this operation is `POST /v1/opportunities/:opportunity_id/convert-to-client` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-opportunity-to-client.md) for the provider-specific parameters and requirements.

