# Teamgate: List Deal People

Retrieves people for a deal in Teamgate.

```
GET https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-deal-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-deal-people?connectionId=$CONNECTION_ID&dealId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dealId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-deal-people?${params}`, {
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
| `dealId` | string | yes | Deal ID whose linked people should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "isDeleted": "string",
      "name": "Ava Chen",
      "surname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isDeleted` | string |  |
| `name` | string |  |
| `surname` | string |  |

## Native endpoint

Through the native Teamgate API, this operation is `GET /deals/:deal_id/people` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deal-people.md) for the provider-specific parameters and requirements.

