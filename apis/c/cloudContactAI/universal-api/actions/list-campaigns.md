# CloudContactAI: List Campaigns



```
GET https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/list-campaigns?${params}`, {
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
| `pageNumber` | number | no | The page number. |
| `pageSize` | number | no | The page size. |
| `term` | string | no | Optional search term. |
| `offset` | number | no | Optional result offset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {},
      "clientId": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isDefault": true,
      "message": "string",
      "stats": {},
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `clientId` | number |  |
| `createdDate` | date |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `message` | string |  |
| `stats` | object |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `GET api/v2/campaigns` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

