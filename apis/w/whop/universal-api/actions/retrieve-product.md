# Whop: Retrieve Product

Retrieves product details from the Whop platform.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-product?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-product?${params}`, {
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
| `id` | string | yes | The unique identifier of the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "id": "string",
        "route": "string",
        "title": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customCta": "string",
      "galleryImages": [
        {
          "id": "string",
          "url": "https://example.com"
        }
      ],
      "globalAffiliatePercentage": 1,
      "globalAffiliateStatus": "string",
      "id": "string",
      "memberAffiliatePercentage": 1,
      "memberAffiliateStatus": "string",
      "memberCount": 1,
      "ownerUser": {
        "id": "string",
        "name": "Ava Chen",
        "username": "Ava Chen"
      },
      "publishedReviewsCount": 1,
      "route": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "verified": true,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `company.id` | string |  |
| `company.route` | string |  |
| `company.title` | string |  |
| `createdAt` | date |  |
| `customCta` | string |  |
| `galleryImages` | array<object> |  |
| `galleryImages[].id` | string |  |
| `galleryImages[].url` | string |  |
| `globalAffiliatePercentage` | number |  |
| `globalAffiliateStatus` | string |  |
| `id` | string |  |
| `memberAffiliatePercentage` | number |  |
| `memberAffiliateStatus` | string |  |
| `memberCount` | number |  |
| `ownerUser` | object |  |
| `ownerUser.id` | string |  |
| `ownerUser.name` | string |  |
| `ownerUser.username` | string |  |
| `publishedReviewsCount` | number |  |
| `route` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `verified` | boolean |  |
| `visibility` | string |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/products/:id` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-product.md) for the provider-specific parameters and requirements.

