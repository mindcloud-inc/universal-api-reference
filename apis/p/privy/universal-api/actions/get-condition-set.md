# Privy: Get Condition Set

Retrieves a condition set from Privy.

```
GET https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-condition-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-condition-set?connectionId=$CONNECTION_ID&conditionSetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conditionSetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-condition-set?${params}`, {
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
      "created_at": 1,
      "id": "string",
      "name": "Ava Chen",
      "owner_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `id` | string |  |
| `name` | string |  |
| `owner_id` | string |  |

## Native endpoint

Through the native Privy API, this operation is `GET /v1/condition_sets/{{conditionSetId}}` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-condition-set.md) for the provider-specific parameters and requirements.

