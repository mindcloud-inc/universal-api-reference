# OneSuite: List Company People

Retrieves a company's people from OneSuite.

```
GET https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-company-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-company-people?connectionId=$CONNECTION_ID&companyId=cmo7gu3gq02robo05g27zy4n0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "cmo7gu3gq02robo05g27zy4n0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-company-people?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes | Company ID from the OneSuite company-people docs. Example: `cmo7gu3gq02robo05g27zy4n0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneSuite API returns.

## Native endpoint

Through the native OneSuite API, this operation is `GET /v1/companies/:company_id/people` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-people.md) for the provider-specific parameters and requirements.

