# Bulldog-WP: Validate numbers

Validates phone numbers in Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/validate-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/validate-numbers?connectionId=$CONNECTION_ID&numbers%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "numbers[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/validate-numbers?${params}`, {
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
| `numbers[]` | array<object> | yes | List of phone numbers to validate and normalize. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "numbers": [
        {}
      ],
      "summary": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `numbers` | array<object> |  |
| `summary` | object |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `POST /numbers/validate` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-numbers.md) for the provider-specific parameters and requirements.

