# Privy: Delete Policy Rule

Deletes a rule from a Privy policy.

```
DELETE https://connect.mindcloud.co/v1/universal/privy/latest/actions/delete-policy-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/privy/latest/actions/delete-policy-rule?connectionId=$CONNECTION_ID&policyId=string&ruleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "policyId": "string",
  "ruleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/delete-policy-rule?${params}`, {
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
| `policyId` | string | yes | Privy policy ID. |
| `ruleId` | string | yes | Privy policy rule ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Privy API, this operation is `DELETE /v1/policies/{{policyId}}/rules/{{ruleId}}` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-policy-rule.md) for the provider-specific parameters and requirements.

