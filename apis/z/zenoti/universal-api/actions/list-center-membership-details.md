# Zenoti: List Center Membership Details



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-center-membership-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-center-membership-details?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-center-membership-details?${params}`, {
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
| `centerId` | list | no |  |
| `status` | list | no |  |
| `createdDate` | date | no |  |
| `lastUpdatedDate` | date | no |  |
| `returnOnlyTotal` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelledDate": "2026-05-07T12:00:00.000Z",
      "closedDate": "2026-05-07T12:00:00.000Z",
      "creditsAmount": 1,
      "endDate": "2026-05-07T12:00:00.000Z",
      "freezeDate": "2026-05-07T12:00:00.000Z",
      "guest": {
        "code": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "membership": {
        "code": "string",
        "id": "string",
        "name": "Ava Chen",
        "type": "string",
        "versionId": "string"
      },
      "productsAmount": 1,
      "recurrenceStatus": "string",
      "renewalDetails": "string",
      "servicesAmount": 1,
      "soldDate": "2026-05-07T12:00:00.000Z",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelledDate` | date |  |
| `closedDate` | date |  |
| `creditsAmount` | number |  |
| `endDate` | date |  |
| `freezeDate` | date |  |
| `guest.code` | string |  |
| `guest.id` | string |  |
| `guest.name` | string |  |
| `id` | string |  |
| `membership.code` | string |  |
| `membership.id` | string |  |
| `membership.name` | string |  |
| `membership.type` | string |  |
| `membership.versionId` | string |  |
| `productsAmount` | number |  |
| `recurrenceStatus` | string |  |
| `renewalDetails` | string |  |
| `servicesAmount` | number |  |
| `soldDate` | date |  |
| `startDate` | date |  |
| `status` | string |  |

## Native endpoint

Through the native Zenoti API, this operation is `GET centers/:centerId/members` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-center-membership-details.md) for the provider-specific parameters and requirements.

