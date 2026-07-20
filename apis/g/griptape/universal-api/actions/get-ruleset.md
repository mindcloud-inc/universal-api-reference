# Griptape: Get Ruleset

Retrieves a ruleset from Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-ruleset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-ruleset?connectionId=$CONNECTION_ID&rulesetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rulesetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-ruleset?${params}`, {
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
| `rulesetId` | string | yes | The Griptape ruleset ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "created_at": "string",
      "created_by": "string",
      "description": "string",
      "metadata": {},
      "name": "Ava Chen",
      "organization_id": "string",
      "rule_ids": [
        "string"
      ],
      "ruleset_id": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `created_at` | string |  |
| `created_by` | string |  |
| `description` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `organization_id` | string |  |
| `rule_ids` | array<string> |  |
| `ruleset_id` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Griptape API, this operation is `GET /api/rulesets/:ruleset_id` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ruleset.md) for the provider-specific parameters and requirements.

