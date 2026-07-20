# Privy: List Condition Set Items

Retrieves items from a Privy condition set.

```
GET https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-condition-set-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-condition-set-items?connectionId=$CONNECTION_ID&conditionSetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conditionSetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-condition-set-items?${params}`, {
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
| `conditionSetId` | string | yes | Privy condition set ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "condition_set_id": "string",
          "created_at": 1,
          "id": "string",
          "value": "string"
        }
      ],
      "next_cursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].condition_set_id` | string |  |
| `items[].created_at` | number |  |
| `items[].id` | string |  |
| `items[].value` | string |  |
| `next_cursor` | string |  |

## Native endpoint

Through the native Privy API, this operation is `GET /v1/condition_sets/{{conditionSetId}}/condition_set_items` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-condition-set-items.md) for the provider-specific parameters and requirements.

