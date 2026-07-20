# Reward Sciences: Get Reward



```
GET https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/get-reward
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reward Sciences `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/get-reward?connectionId=$CONNECTION_ID&rewardId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rewardId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/get-reward?${params}`, {
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
| `rewardId` | number | yes | The Reward Sciences reward ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "image": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Reward description when present. |
| `id` | number | Reward ID. |
| `image` | string | Reward image URL when present. |
| `name` | string | Reward name when present. |

## Native endpoint

Through the native Reward Sciences API, this operation is `GET /rewards/:rewardId` (base URL `https://api.rewardsciences.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reward.md) for the provider-specific parameters and requirements.

