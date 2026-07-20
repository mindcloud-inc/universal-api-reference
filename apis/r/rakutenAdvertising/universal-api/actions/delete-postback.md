# Rakuten Advertising: Delete postback

Deletes an existing postback from Rakuten Advertising.

```
DELETE https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/delete-postback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/delete-postback?connectionId=$CONNECTION_ID&publisherId=4693234" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publisherId": "4693234"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/delete-postback?${params}`, {
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
| `publisherId` | string | yes | Rakuten publisher SID. Default: `4693234`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "message": "string",
      "publisherId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `message` | string |  |
| `publisherId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `DELETE /v1/postback/{publisherId}` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-postback.md) for the provider-specific parameters and requirements.

