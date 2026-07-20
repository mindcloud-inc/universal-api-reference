# Curator: Delete Ad

Deletes an existing ad or custom post from Curator.

```
DELETE https://connect.mindcloud.co/v1/universal/curator/latest/actions/delete-ad
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Curator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/curator/latest/actions/delete-ad?connectionId=$CONNECTION_ID&adId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/curator/latest/actions/delete-ad?${params}`, {
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
| `adId` | string | yes | ID of the ad to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": true,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native Curator API, this operation is `DELETE /v1.2/ads/:AD_ID` (base URL `https://api.curator.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-ad.md) for the provider-specific parameters and requirements.

