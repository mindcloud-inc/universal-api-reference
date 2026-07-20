# ironSource: Delete Placement

Deletes an existing placement from ironSource by archiving it.

```
DELETE https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/delete-placement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ironSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/delete-placement?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/delete-placement?${params}`, {
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
| `adUnit` | string | no | Ad unit name: rewardedVideo, interstitial, or banner. |
| `appKey` | string | no | Application key to archive the placement for. |
| `id` | string | no | Placement ID to archive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | True when the archive request succeeds with HTTP 200. |

## Native endpoint

Through the native ironSource API, this operation is `DELETE partners/publisher/placements/v1` (base URL `https://platform.ironsrc.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-placement.md) for the provider-specific parameters and requirements.

