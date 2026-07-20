# Pinterest: Create Pin

Creates a new pin in Pinterest.

```
POST https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/create-pin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinterest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/create-pin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/create-pin', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `altText` | string | no |  |
| `board` | list | no |  |
| `boardSectionId` | string | no |  |
| `description` | string | no |  |
| `dominantColor` | string | no |  |
| `link` | string | no |  |
| `note` | string | no |  |
| `parentPinId` | string | no |  |
| `title` | string | no |  |
| `carouselSlides[].altText` | string | no |  |
| `mediasource.items[].title` | string | no |  |
| `mediaSource.items[].title` | string | no |  |
| `mediasource.sourcetype` | list | no |  |
| `mediaSource.sourceType` | list | no |  |
| `product.price.currency` | string | no |  |
| `product.productLink` | string | no |  |
| `carouselSlides[].title` | string | no |  |
| `mediasource.items[]` | array | no |  |
| `mediaSource.items[]` | array | no |  |
| `mediaSource.items[].contentType` | string | no |  |
| `mediasource.items[].description` | string | no |  |
| `product.price.amount` | string | no |  |
| `product.productId` | string | no |  |
| `carouselSlides[].description` | string | no |  |
| `mediaSource.items[].data` | string | no |  |
| `mediasource.items[].link` | string | no |  |
| `product.price` | object | no |  |
| `mediaSource.items[].link` | string | no |  |
| `mediasource.items[].url` | string | no |  |
| `product.availability` | string | no |  |
| `mediaSource.items[].description` | string | no |  |
| `mediasource.items[].index` | string | no |  |
| `product.itemGroupId` | string | no |  |
| `mediaSource.items[].url` | string | no |  |
| `mediaSource` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinterest API returns.

## Native endpoint

Through the native Pinterest API, this operation is `POST pins` (base URL `https://api.pinterest.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pin.md) for the provider-specific parameters and requirements.

