# Moosend: List Segments

Retrieves segments from Moosend.

```
GET https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-segments?connectionId=$CONNECTION_ID&mailingListId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailingListId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-segments?${params}`, {
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
| `mailingListId` | string | yes | The ID of the email list that contains the segments. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "criteria": [
        {}
      ],
      "description": "string",
      "fetchType": 1,
      "fetchValue": 1,
      "id": 1,
      "matchType": 1,
      "name": "Ava Chen",
      "segmentType": 1,
      "updatedBy": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string |  |
| `createdOn` | date |  |
| `criteria` | array<object> |  |
| `description` | string |  |
| `fetchType` | number |  |
| `fetchValue` | number |  |
| `id` | number |  |
| `matchType` | number |  |
| `name` | string |  |
| `segmentType` | number |  |
| `updatedBy` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Moosend API, this operation is `GET /lists/{{MailingListID}}/segments.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segments.md) for the provider-specific parameters and requirements.

