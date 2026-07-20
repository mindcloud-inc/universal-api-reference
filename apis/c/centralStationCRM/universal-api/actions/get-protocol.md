# CentralStationCRM: Get Protocol

Retrieves a single protocol from CentralStationCRM.

```
GET https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/get-protocol
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CentralStationCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/get-protocol?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/get-protocol?${params}`, {
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
      "accountId": 1,
      "attachmentsCount": 1,
      "badge": "string",
      "commentsCount": 1,
      "companyId": 1,
      "companyIds": [
        1
      ],
      "confidential": true,
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dataHash": {},
      "dealIds": [
        1
      ],
      "format": "string",
      "id": 1,
      "name": "Ava Chen",
      "occurredAt": "2026-05-07T12:00:00.000Z",
      "personId": 1,
      "personIds": [
        1
      ],
      "projectIds": [
        1
      ],
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedByUserId": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `attachmentsCount` | number |  |
| `badge` | string |  |
| `commentsCount` | number |  |
| `companyId` | number |  |
| `companyIds` | array<number> |  |
| `confidential` | boolean |  |
| `content` | string |  |
| `createdAt` | date |  |
| `dataHash` | object |  |
| `dealIds` | array<number> |  |
| `format` | string |  |
| `id` | number |  |
| `name` | string |  |
| `occurredAt` | date |  |
| `personId` | number |  |
| `personIds` | array<number> |  |
| `projectIds` | array<number> |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `updatedByUserId` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native CentralStationCRM API, this operation is `GET /api/protocols/:id` (base URL `https://api.centralstationcrm.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-protocol.md) for the provider-specific parameters and requirements.

