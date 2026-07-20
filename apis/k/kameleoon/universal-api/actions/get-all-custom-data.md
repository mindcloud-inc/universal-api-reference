# Kameleoon: Get all custom data



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-custom-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-custom-data?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-custom-data?${params}`, {
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
      "description": "string",
      "id": 1,
      "index": 1,
      "isConstant": true,
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "siteId": 1,
      "tags": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date |  |
| `description` | string |  |
| `id` | number |  |
| `index` | number |  |
| `isConstant` | boolean |  |
| `modificationDate` | date |  |
| `name` | string |  |
| `siteId` | number |  |
| `tags` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native Kameleoon API, this operation is `GET custom-datas` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-custom-data.md) for the provider-specific parameters and requirements.

