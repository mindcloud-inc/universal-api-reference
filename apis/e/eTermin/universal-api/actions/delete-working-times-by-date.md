# eTermin: Delete Working Times by Date

Deletes working times by date from eTermin.

```
DELETE https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/delete-working-times-by-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/delete-working-times-by-date?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/delete-working-times-by-date?${params}`, {
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
| `calendarid` | number | no | ID of the calendar, every working slot for specific days will be deleted |
| `id` | number | no | ID of the working time that needs to be deleted |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "statusmsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |
| `statusmsg` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `DELETE /api/workingtimesdate` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-working-times-by-date.md) for the provider-specific parameters and requirements.

