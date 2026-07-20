# Kameleoon: Get all key pages



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-key-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-key-pages?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-key-pages?${params}`, {
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
| `paramsIo` | string | yes | Required query object documented by Kameleoon for list endpoints. Example: `page=1, perPage=20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "matchType": "string",
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "relativeUrlRegExp": "https://example.com",
      "secondMatchType": "string",
      "siteId": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date |  |
| `id` | number |  |
| `matchType` | string |  |
| `modificationDate` | date |  |
| `name` | string |  |
| `relativeUrlRegExp` | string |  |
| `secondMatchType` | string |  |
| `siteId` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Kameleoon API, this operation is `GET key-pages` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-key-pages.md) for the provider-specific parameters and requirements.

