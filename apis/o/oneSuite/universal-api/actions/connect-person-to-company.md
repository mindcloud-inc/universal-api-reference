# OneSuite: Connect Person to Company

Connects a person to a company in OneSuite.

```
PUT https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/connect-person-to-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/connect-person-to-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "peopleId": "cmo7gy9qu02s8bo05g4fdcwqw",
  "companyId": "cmo7gzxna02smbo056u59sb9y"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/connect-person-to-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "peopleId": "cmo7gy9qu02s8bo05g4fdcwqw",
    "companyId": "cmo7gzxna02smbo056u59sb9y"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `peopleId` | string | yes | People ID from the connect-people-to-company docs. Example: `cmo7gy9qu02s8bo05g4fdcwqw`. |
| `companyId` | string | yes | Company ID to connect to the person. Example: `cmo7gzxna02smbo056u59sb9y`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneSuite API returns.

## Native endpoint

Through the native OneSuite API, this operation is `POST /v1/people/:people_id/company` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connect-person-to-company.md) for the provider-specific parameters and requirements.

