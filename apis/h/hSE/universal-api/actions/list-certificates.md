# 4HSE: List Certificates

Retrieves certificates from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-certificates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-certificates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-certificates?${params}`, {
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
      "actionType": "string",
      "certificateId": "string",
      "dateExpire": "2026-05-07T12:00:00.000Z",
      "dateRelease": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "permission": "string",
      "resourceId": "string",
      "resourceName": "Ava Chen",
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionType` | string | Certificate action type |
| `certificateId` | string | Certificate identifier |
| `dateExpire` | date | Expiry date |
| `dateRelease` | date | Release date |
| `name` | string | Certificate name |
| `permission` | string | Permission level |
| `resourceId` | string | Resource identifier |
| `resourceName` | string | Resource name |
| `tenantId` | string | Project identifier |

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/certificate/index` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-certificates.md) for the provider-specific parameters and requirements.

