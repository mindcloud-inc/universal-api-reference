# Griptape: List Rules In Ruleset

Finds rules in a Griptape ruleset.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-rules-in-ruleset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-rules-in-ruleset?connectionId=$CONNECTION_ID&rulesetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rulesetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-rules-in-ruleset?${params}`, {
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
| `rulesetId` | string | yes | Filter rules to a specific ruleset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "page_number": 1,
        "page_size": 1,
        "total_count": 1,
        "total_pages": 1
      },
      "rules": [
        {
          "created_at": "string",
          "created_by": "string",
          "metadata": {},
          "name": "Ava Chen",
          "organization_id": "string",
          "rule": "string",
          "rule_id": "string",
          "updated_at": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.page_number` | number |  |
| `pagination.page_size` | number |  |
| `pagination.total_count` | number |  |
| `pagination.total_pages` | number |  |
| `rules[].created_at` | string |  |
| `rules[].created_by` | string |  |
| `rules[].metadata` | object |  |
| `rules[].name` | string |  |
| `rules[].organization_id` | string |  |
| `rules[].rule` | string |  |
| `rules[].rule_id` | string |  |
| `rules[].updated_at` | string |  |

## Native endpoint

Through the native Griptape API, this operation is `GET /api/rules` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rules-in-ruleset.md) for the provider-specific parameters and requirements.

