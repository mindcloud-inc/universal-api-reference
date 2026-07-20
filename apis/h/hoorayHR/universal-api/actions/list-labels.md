# HoorayHR: List Labels

Retrieves label records from the HoorayHR account.

```
GET https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoorayHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-labels?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "documentCategoryId": 1,
      "id": 1,
      "name": {},
      "systemCategoryType": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workflowCategoryId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `documentCategoryId` | number |  |
| `id` | number |  |
| `name` | object |  |
| `systemCategoryType` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `workflowCategoryId` | number |  |

## Native endpoint

Through the native HoorayHR API, this operation is `GET /labels` (base URL `https://api.hoorayhr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-labels.md) for the provider-specific parameters and requirements.

