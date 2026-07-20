# GoodDay.work: List User Hourly Rate History

Retrieves hourly rate history from GoodDay.work for a user.

```
GET https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-user-hourly-rate-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-user-hourly-rate-history?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-user-hourly-rate-history?${params}`, {
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
| `userId` | string | yes | GoodDay user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fromDate": "string",
      "hourlyRate": 1,
      "toDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fromDate` | string | Effective-from date. |
| `hourlyRate` | number | Hourly rate value. |
| `toDate` | string | Effective-to date. |

## Native endpoint

Through the native GoodDay.work API, this operation is `GET /user/:userId/hourly-rate-history` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-hourly-rate-history.md) for the provider-specific parameters and requirements.

