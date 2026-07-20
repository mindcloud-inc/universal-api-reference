# Yeti Snow: Get Site



```
GET https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yeti Snow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-site?${params}`, {
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
| `siteId` | string | no | Site identifier from List Sites. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the site is active. |
| `id` | string | Site identifier. |
| `name` | string | Site name. |

## Native endpoint

Through the native Yeti Snow API, this operation is `GET site/show` (base URL `https://sandbox_api.yetisoftware.com/api/en/public_access/1715`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

