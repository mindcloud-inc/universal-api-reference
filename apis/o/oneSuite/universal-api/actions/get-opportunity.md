# OneSuite: Get Opportunity

Retrieves an opportunity from OneSuite.

```
GET https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-opportunity?connectionId=$CONNECTION_ID&opportunityId=cmo7h1vjm02stbo05mhgr2rmy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "opportunityId": "cmo7h1vjm02stbo05mhgr2rmy"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-opportunity?${params}`, {
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
| `opportunityId` | string | yes | Opportunity ID from the OneSuite single-opportunity docs. Example: `cmo7h1vjm02stbo05mhgr2rmy`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneSuite API returns.

## Native endpoint

Through the native OneSuite API, this operation is `GET /v1/opportunities/:opportunity_id` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-opportunity.md) for the provider-specific parameters and requirements.

