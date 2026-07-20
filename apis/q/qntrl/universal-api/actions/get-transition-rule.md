# Qntrl: Get Transition Rule

Retrieves a transition rule from Qntrl.

```
GET https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/get-transition-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qntrl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/get-transition-rule?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qntrl/latest/actions/get-transition-rule?${params}`, {
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
| `org_id` | string | no | Qntrl organization ID. |
| `transition_rule_id` | string | no | Qntrl transition rule ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "name": "Ava Chen",
      "ruleId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `name` | string |  |
| `ruleId` | string |  |

## Native endpoint

Through the native Qntrl API, this operation is `GET /[:org_id]/transitionrule/[:transition_rule_id]` (base URL `https://coreapi.qntrl.com/blueprint/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transition-rule.md) for the provider-specific parameters and requirements.

