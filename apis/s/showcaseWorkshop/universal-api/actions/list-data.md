# Showcase Workshop: List Data

Retrieves data items from Showcase Workshop.

```
GET https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/list-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Showcase Workshop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/list-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/list-data?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromDate` | date | no | Return data added after this ISO 8601 date/time. Example: `2013-11-26T00:26:54Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "dataName": "Ava Chen",
      "dataType": "string",
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
| `content` | string | Stored content payload. |
| `dataName` | string | Name of the data item or form. |
| `dataType` | string | Source type for the data item. |
| `dateInserted` | date | Date/time the data item was inserted. |
| `dateUpdated` | date | Date/time the data item was last updated. |
| `guid` | string | Unique identifier for the data item. |
| `showcaseId` | number | Numeric Showcase identifier. |
| `showcaseName` | string | Showcase name. |
| `userEmail` | string | Email for the user associated with the data. |
| `userFirstName` | string |  |
| `userId` | number | Numeric Showcase user identifier. |
| `userLastName` | string |  |

## Native endpoint

Through the native Showcase Workshop API, this operation is `GET /data/` (base URL `https://app.showcaseworkshop.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data.md) for the provider-specific parameters and requirements.

