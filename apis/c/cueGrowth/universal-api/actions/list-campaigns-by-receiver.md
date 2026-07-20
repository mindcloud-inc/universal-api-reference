# CueGrowth: List Campaigns by Receiver



```
GET https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/list-campaigns-by-receiver
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CueGrowth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/list-campaigns-by-receiver?connectionId=$CONNECTION_ID&receiverId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "receiverId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/list-campaigns-by-receiver?${params}`, {
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
| `receiverId` | string | yes | ID of the receiver. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native CueGrowth API, this operation is `GET /campaigns/get_all_by_receiver/{receiver_id}` (base URL `https://api.cuegrowth.ai/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns-by-receiver.md) for the provider-specific parameters and requirements.

