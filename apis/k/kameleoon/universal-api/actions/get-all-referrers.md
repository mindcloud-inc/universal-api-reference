# Kameleoon: Get all referrers



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-referrers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-referrers?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-referrers?${params}`, {
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
      "detections": [
        {}
      ],
      "id": 1,
      "index": 1,
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "priority": 1,
      "siteId": 1,
      "tags": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date |  |
| `detections` | array<object> |  |
| `id` | number |  |
| `index` | number |  |
| `modificationDate` | date |  |
| `name` | string |  |
| `priority` | number |  |
| `siteId` | number |  |
| `tags` | string |  |

## Native endpoint

Through the native Kameleoon API, this operation is `GET referrers` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-referrers.md) for the provider-specific parameters and requirements.

