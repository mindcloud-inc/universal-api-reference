# 4HSE: List Certificate Action Links

Retrieves certificate-action links from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-certificate-action-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-certificate-action-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-certificate-action-links?${params}`, {
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
      "actionCode": "string",
      "actionId": "string",
      "actionName": "Ava Chen",
      "actionType": "string",
      "certificateActionId": "string",
      "certificateId": "string",
      "certificateName": "Ava Chen",
      "dateExpire": "2026-05-07T12:00:00.000Z",
      "dateRelease": "2026-05-07T12:00:00.000Z",
      "isDateInherited": 1,
      "officeId": "string",
      "officeName": "Ava Chen",
      "permission": "string",
      "resourceId": "string",
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionCode` | string | Action code |
| `actionId` | string | Action identifier |
| `actionName` | string | Action name |
| `actionType` | string | Action type |
| `certificateActionId` | string | Certificate action link identifier |
| `certificateId` | string | Certificate identifier |
| `certificateName` | string | Certificate name |
| `dateExpire` | date | Expiry date |
| `dateRelease` | date | Release date |
| `isDateInherited` | number | Whether expiry date is inherited |
| `officeId` | string | Office identifier |
| `officeName` | string | Office name |
| `permission` | string | Permission level |
| `resourceId` | string | Resource identifier |
| `tenantId` | string | Project identifier |

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/certificate-action/index` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-certificate-action-links.md) for the provider-specific parameters and requirements.

