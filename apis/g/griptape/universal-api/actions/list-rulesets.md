# Griptape: List Rulesets

Finds rulesets in Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-rulesets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-rulesets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-rulesets?${params}`, {
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
| `alias` | string | no | Optional alias to filter the ruleset list. |

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
      "rulesets": [
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
| `rulesets[].alias` | string |  |
| `rulesets[].created_at` | string |  |
| `rulesets[].created_by` | string |  |
| `rulesets[].description` | string |  |
| `rulesets[].metadata` | object |  |
| `rulesets[].name` | string |  |
| `rulesets[].organization_id` | string |  |
| `rulesets[].rule_ids` | array<string> |  |
| `rulesets[].ruleset_id` | string |  |
| `rulesets[].updated_at` | string |  |

## Native endpoint

Through the native Griptape API, this operation is `GET /api/rulesets` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rulesets.md) for the provider-specific parameters and requirements.

