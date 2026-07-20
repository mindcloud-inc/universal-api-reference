# Expensify: Get Policies

Retrieves specific policies from Expensify.

```
GET https://connect.mindcloud.co/v1/universal/expensify/latest/actions/get-policies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/get-policies?connectionId=$CONNECTION_ID&policyIdList=string&fields=categories%2Ctags%2Ctax" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "policyIdList": "string",
  "fields": "categories,tags,tax"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expensify/latest/actions/get-policies?${params}`, {
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
| `policyIdList` | string | yes | Comma-separated Expensify policy IDs to fetch. |
| `fields` | string | yes | Comma-separated policy fields to return: categories, reportFields, tags, tax, employees. Default: `categories,tags,tax`. |
| `userEmail` | string | no | Optional user email for third-party accessible domain policy data. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Expensify API returns.

## Native endpoint

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-policies.md) for the provider-specific parameters and requirements.

