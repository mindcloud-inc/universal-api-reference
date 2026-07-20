# Umbrella: Delete Alert Rules

Deletes existing alert rules from Umbrella.

```
DELETE https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/delete-alert-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbrella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/delete-alert-rules?connectionId=$CONNECTION_ID&ruleIds=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ruleIds": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/delete-alert-rules?${params}`, {
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
| `ruleIds` | list<number> | yes | A list of alert rule IDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorIds": [
        1
      ],
      "success": true,
      "successfulIds": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorIds` | array<number> |  |
| `success` | boolean |  |
| `successfulIds` | array<number> |  |

## Native endpoint

Through the native Umbrella API, this operation is `DELETE https://api.sse.cisco.com/admin/v2/alerting/rules` (base URL `https://api.umbrella.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-alert-rules.md) for the provider-specific parameters and requirements.

