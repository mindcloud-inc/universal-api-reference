# Statsig: Delete Gate Rule

Deletes a gate rule from Statsig.

```
DELETE https://connect.mindcloud.co/v1/universal/statsig/latest/actions/delete-gate-rule-delete-console-v1-gates-id-rules-ruleid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/delete-gate-rule-delete-console-v1-gates-id-rules-ruleid?connectionId=$CONNECTION_ID&id=string&ruleID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "ruleID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/delete-gate-rule-delete-console-v1-gates-id-rules-ruleid?${params}`, {
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
| `id` | string | yes | Gate ID |
| `ruleID` | string | yes | Rule ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `DELETE /console/v1/gates/{id}/rules/{ruleID}` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-gate-rule-delete-console-v1-gates-id-rules-ruleid.md) for the provider-specific parameters and requirements.

