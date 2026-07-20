# ActivityInfo: Get Database Billing Account

Retrieves a database's billing account from ActivityInfo.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-database-billing-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-database-billing-account?connectionId=$CONNECTION_ID&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-database-billing-account?${params}`, {
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
| `databaseId` | string | yes | ActivityInfo database ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "databaseCount": 1,
      "id": 1,
      "name": "Ava Chen",
      "planName": "Ava Chen",
      "status": "string",
      "trial": true,
      "userCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Subscription code. |
| `databaseCount` | number | Current database count. |
| `id` | number | Billing account ID. |
| `name` | string | Billing account name. |
| `planName` | string | Plan name. |
| `status` | string | Billing account status. |
| `trial` | boolean | Whether this is a trial account. |
| `userCount` | number | Current unique invited user count. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/databases/:databaseId/billingAccount` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database-billing-account.md) for the provider-specific parameters and requirements.

