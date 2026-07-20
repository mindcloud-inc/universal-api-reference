# Adyntel: Get TikTok Ad Details

Retrieves TikTok ad details from Adyntel by ad ID.

```
GET https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/get-tik-tok-ad-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adyntel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/get-tik-tok-ad-details?connectionId=$CONNECTION_ID&id=74827364827364" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "74827364827364"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/get-tik-tok-ad-details?${params}`, {
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
| `id` | string | yes | TikTok ad ID. Example: `74827364827364`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |

## Native endpoint

Through the native Adyntel API, this operation is `POST /tiktok_ad_details` (base URL `https://api.adyntel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tik-tok-ad-details.md) for the provider-specific parameters and requirements.

