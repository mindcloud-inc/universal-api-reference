# HoorayHR: List Contracts

Retrieves employment contract records from HoorayHR.

```
GET https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoorayHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-contracts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-contracts?${params}`, {
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
      "contractEndDate": "string",
      "contractStartDate": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "labels": [
        {}
      ],
      "probationEndDate": "2026-05-07T12:00:00.000Z",
      "signedContract": 1,
      "status": "string",
      "type": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "userIdApproved": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contractEndDate` | string |  |
| `contractStartDate` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `labels` | array<object> |  |
| `probationEndDate` | date |  |
| `signedContract` | number |  |
| `status` | string |  |
| `type` | number |  |
| `updatedAt` | date |  |
| `userId` | number |  |
| `userIdApproved` | number |  |

## Native endpoint

Through the native HoorayHR API, this operation is `GET /contracts` (base URL `https://api.hoorayhr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contracts.md) for the provider-specific parameters and requirements.

