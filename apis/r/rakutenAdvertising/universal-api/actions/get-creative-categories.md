# Rakuten Advertising: Get creative categories

Retrieves creative categories from Rakuten Advertising.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-creative-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-creative-categories?connectionId=$CONNECTION_ID&advertiserId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "advertiserId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/get-creative-categories?${params}`, {
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
| `advertiserId` | string | yes | Rakuten advertiser ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "advertiserId": "string",
      "categoryId": "string",
      "name": "Ava Chen",
      "rawXml": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advertiserId` | string |  |
| `categoryId` | string |  |
| `name` | string |  |
| `rawXml` | string |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `GET /linklocator/1.0/getCreativeCategories/{advertiserId}` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-creative-categories.md) for the provider-specific parameters and requirements.

