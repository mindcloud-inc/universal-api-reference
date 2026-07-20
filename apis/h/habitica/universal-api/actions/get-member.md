# Habitica: Get Member

Retrieves a member from Habitica.

```
GET https://connect.mindcloud.co/v1/universal/habitica/latest/actions/get-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Habitica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/habitica/latest/actions/get-member?connectionId=$CONNECTION_ID&memberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "memberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/habitica/latest/actions/get-member?${params}`, {
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
| `memberId` | string | yes | The Habitica member ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "party": {},
      "preferences": {},
      "profile": {},
      "stats": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `party` | object |  |
| `preferences` | object |  |
| `profile` | object |  |
| `stats` | object |  |

## Native endpoint

Through the native Habitica API, this operation is `GET /members/:memberId` (base URL `https://habitica.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member.md) for the provider-specific parameters and requirements.

