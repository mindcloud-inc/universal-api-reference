# Middesk: Retrieve website analysis for a business

Retrieves website analysis for a business in Middesk.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-business-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-business-website?connectionId=$CONNECTION_ID&businessId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-business-website?${params}`, {
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
| `businessId` | string | yes | ID of the business whose website analysis you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "businessId": "string",
      "businessNameMatch": true,
      "category": "string",
      "createdAt": "string",
      "description": "string",
      "domain": {},
      "emailAddresses": [
        {}
      ],
      "error": "string",
      "httpStatusCode": 1,
      "id": "string",
      "names": [
        {}
      ],
      "object": "string",
      "pages": [
        {}
      ],
      "parked": true,
      "people": [
        {}
      ],
      "phoneNumbers": [
        {}
      ],
      "platform": "string",
      "postsSummary": "string",
      "rating": {},
      "reviewsSummary": "string",
      "status": "string",
      "submitted": true,
      "title": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `businessId` | string |  |
| `businessNameMatch` | boolean |  |
| `category` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `domain` | object |  |
| `emailAddresses` | array<object> |  |
| `error` | string |  |
| `httpStatusCode` | number |  |
| `id` | string |  |
| `names` | array<object> |  |
| `object` | string |  |
| `pages` | array<object> |  |
| `parked` | boolean |  |
| `people` | array<object> |  |
| `phoneNumbers` | array<object> |  |
| `platform` | string |  |
| `postsSummary` | string |  |
| `rating` | object |  |
| `reviewsSummary` | string |  |
| `status` | string |  |
| `submitted` | boolean |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `GET /businesses/:business_id/website` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-business-website.md) for the provider-specific parameters and requirements.

