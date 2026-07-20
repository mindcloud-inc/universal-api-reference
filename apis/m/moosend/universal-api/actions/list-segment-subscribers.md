# Moosend: List Segment Subscribers

Retrieves segment subscribers from Moosend.

```
GET https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-segment-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-segment-subscribers?connectionId=$CONNECTION_ID&mailingListId=string&segmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailingListId": "string",
  "segmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-segment-subscribers?${params}`, {
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
| `mailingListId` | string | yes | The ID of the email list that contains the segment. |
| `segmentId` | string | yes | The ID of the segment that contains the subscribers you are requesting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "removedOn": "string",
      "subscribeMethod": 1,
      "subscribeType": 1,
      "unsubscribedFromID": "string",
      "unsubscribedOn": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | date |  |
| `customFields` | array<object> |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `removedOn` | string |  |
| `subscribeMethod` | number |  |
| `subscribeType` | number |  |
| `unsubscribedFromID` | string |  |
| `unsubscribedOn` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Moosend API, this operation is `GET /lists/{{MailingListID}}/segments/{{SegmentID}}/members.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segment-subscribers.md) for the provider-specific parameters and requirements.

