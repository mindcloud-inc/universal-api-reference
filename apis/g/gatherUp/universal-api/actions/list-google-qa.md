# GatherUp: List Google Q&A

Retrieves Google Q&A entries from GatherUp.

```
GET https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-google-qa
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-google-qa?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-google-qa?${params}`, {
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
| `businessId` | number | no | Business id. |
| `search` | string | no | The string which you are looking for. |
| `locations` | string | no | Business IDs separated by a comma. |
| `status` | string | no | Status questions separated by a comma. |
| `labels` | string | no | User labels separated by a comma. |
| `page` | number | no | Page number Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {}
      ],
      "author": "string",
      "city": "string",
      "content": "string",
      "count": 1,
      "date": "string",
      "errorCode": 1,
      "errorMessage": "string",
      "id": "string",
      "labels": [
        {}
      ],
      "name": "Ava Chen",
      "page": 1,
      "pages": 1,
      "questionId": "string",
      "questions": {},
      "state": "string",
      "status": "string",
      "street_address": "string",
      "total": "string",
      "upvotes": "string",
      "url_desktop": "https://example.com",
      "url_mobile": "https://example.com",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array<object> |  |
| `author` | string |  |
| `city` | string |  |
| `content` | string |  |
| `count` | number |  |
| `date` | string |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |
| `id` | string |  |
| `labels` | array<object> |  |
| `name` | string |  |
| `page` | number |  |
| `pages` | number |  |
| `questionId` | string |  |
| `questions` | object |  |
| `state` | string |  |
| `status` | string |  |
| `street_address` | string |  |
| `total` | string |  |
| `upvotes` | string |  |
| `url_desktop` | string |  |
| `url_mobile` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `GET /google-qa/get` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-google-qa.md) for the provider-specific parameters and requirements.

