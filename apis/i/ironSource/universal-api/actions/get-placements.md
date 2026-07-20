# ironSource: Get Placements

Retrieves placements from ironSource.

```
GET https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-placements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ironSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-placements?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-placements?${params}`, {
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
| `appKey` | string | no | Application key as seen on the LevelPlay platform. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adDelivery": 1,
      "adUnit": "string",
      "capping": {},
      "id": 1,
      "itemName": "Ava Chen",
      "name": "Ava Chen",
      "pacing": {},
      "rewardAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adDelivery` | number | 1 when placement ad delivery is on, otherwise 0. |
| `adUnit` | string | Ad unit name: rewardedVideo, interstitial, or banner. |
| `capping` | object | Capping settings. |
| `id` | number | Placement unique identifier. |
| `itemName` | string | Reward item name for rewarded video placements. |
| `name` | string | Placement unique name. |
| `pacing` | object | Pacing settings. |
| `rewardAmount` | number | Reward amount for a single ad view. |

## Native endpoint

Through the native ironSource API, this operation is `GET partners/publisher/placements/v1` (base URL `https://platform.ironsrc.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-placements.md) for the provider-specific parameters and requirements.

