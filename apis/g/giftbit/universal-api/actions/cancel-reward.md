# Giftbit: Cancel Reward

Cancels an unclaimed reward in Giftbit.

```
DELETE https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/cancel-reward
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giftbit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/cancel-reward?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/cancel-reward?${params}`, {
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
| `uuid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gift": {},
      "info": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gift` | object |  |
| `info` | object |  |
| `status` | number |  |

## Native endpoint

Through the native Giftbit API, this operation is `DELETE /gifts/:uuid` (base URL `https://api-testbed.giftbit.com/papi/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-reward.md) for the provider-specific parameters and requirements.

