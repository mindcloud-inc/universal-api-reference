# Oboloo: List Subcategories

Retrieves subcategories from Oboloo.

```
GET https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-subcategories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oboloo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-subcategories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/list-subcategories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "status": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `deletedAt` | date |  |
| `id` | number |  |
| `status` | number |  |
| `updatedAt` | date |  |
| `value` | string |  |

## Native endpoint

Through the native Oboloo API, this operation is `GET /configuration/getAllSubCategories` (base URL `https://mindcloudwizard20260330.oboloo.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subcategories.md) for the provider-specific parameters and requirements.

