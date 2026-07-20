# Scrapeless: Get Browser Profile

Retrieves a browser profile from Scrapeless.

```
GET https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-browser-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-browser-profile?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-browser-profile?${params}`, {
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
| `profileId` | string | yes | profile id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "name": "Ava Chen",
      "profileId": "string",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | session launching count |
| `name` | string | profile name |
| `profileId` | string | profile id |
| `size` | number | profile size in bytes |

## Native endpoint

Through the native Scrapeless API, this operation is `GET /browser/profiles/:profileId` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-browser-profile.md) for the provider-specific parameters and requirements.

