# White Swan: Policy Search

Retrieves a White Swan policy search by ID.

```
GET https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/policy-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a White Swan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/policy-search?connectionId=$CONNECTION_ID&policySearch=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "policySearch": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/policy-search?${params}`, {
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
| `policySearch` | string | yes | White Swan policy search ID returned by Submit Complete Plan Request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "death_benefit": 1,
      "error_message": "string",
      "goal": "string",
      "linked_plan_request": "https://example.com",
      "policies": {},
      "policies_view_url": "https://example.com",
      "policy_search_id": "string",
      "policy_type": "string",
      "premium_budget": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `death_benefit` | number |  |
| `error_message` | string |  |
| `goal` | string |  |
| `linked_plan_request` | string |  |
| `policies` | object |  |
| `policies_view_url` | string |  |
| `policy_search_id` | string |  |
| `policy_type` | string |  |
| `premium_budget` | number |  |
| `status` | string |  |

## Native endpoint

Through the native White Swan API, this operation is `POST /policy_search` (base URL `https://app.whiteswan.io/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/policy-search.md) for the provider-specific parameters and requirements.

