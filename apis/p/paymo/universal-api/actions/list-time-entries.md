# Paymo: List Time Entries

Retrieves time entries from Paymo.

```
GET https://connect.mindcloud.co/v1/universal/paymo/latest/actions/list-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paymo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paymo/latest/actions/list-time-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paymo/latest/actions/list-time-entries?${params}`, {
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
| `where` | string | no | Optional raw Paymo filtering expression, for example `task_id=32187742`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedManually": true,
      "billed": true,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "date": "string",
      "description": "string",
      "duration": 1,
      "id": 1,
      "isBulk": true,
      "price": 1,
      "projectId": 1,
      "status": "string",
      "taskId": 1,
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedManually` | boolean |  |
| `billed` | boolean |  |
| `createdOn` | date |  |
| `date` | string |  |
| `description` | string |  |
| `duration` | number |  |
| `id` | number |  |
| `isBulk` | boolean |  |
| `price` | number |  |
| `projectId` | number |  |
| `status` | string |  |
| `taskId` | number |  |
| `updatedOn` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native Paymo API, this operation is `GET entries` (base URL `https://app.paymoapp.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-entries.md) for the provider-specific parameters and requirements.

