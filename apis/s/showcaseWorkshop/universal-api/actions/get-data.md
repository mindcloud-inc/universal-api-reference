# Showcase Workshop: Get Data

Retrieves a data item from Showcase Workshop.

```
GET https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/get-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Showcase Workshop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/get-data?connectionId=$CONNECTION_ID&guid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/get-data?${params}`, {
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
| `guid` | string | yes | Unique GUID of the data item to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "dataName": "Ava Chen",
      "dataType": "string",
      "dateEntered": "2026-05-07T12:00:00.000Z",
      "dateInserted": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "guid": "string",
      "showcaseId": 1,
      "showcaseName": "Ava Chen",
      "userEmail": "ava@example.com",
      "userFirstName": "Ava",
      "userId": 1,
      "userLastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `dataName` | string |  |
| `dataType` | string |  |
| `dateEntered` | date |  |
| `dateInserted` | date |  |
| `dateUpdated` | date |  |
| `guid` | string |  |
| `showcaseId` | number |  |
| `showcaseName` | string |  |
| `userEmail` | string |  |
| `userFirstName` | string |  |
| `userId` | number |  |
| `userLastName` | string |  |

## Native endpoint

Through the native Showcase Workshop API, this operation is `GET /data/{guid}` (base URL `https://app.showcaseworkshop.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data.md) for the provider-specific parameters and requirements.

