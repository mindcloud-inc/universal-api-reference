# ActivityInfo: List Billing Account Databases

Retrieves databases for an ActivityInfo billing account.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-billing-account-databases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-billing-account-databases?connectionId=$CONNECTION_ID&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-billing-account-databases?${params}`, {
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
| `accountId` | string | yes | ActivityInfo billing account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingAccountId": 1,
      "databaseId": "string",
      "description": "string",
      "formCount": 1,
      "label": "string",
      "owner": {},
      "recordCount": 1,
      "userCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAccountId` | number | Billing account ID. |
| `databaseId` | string | Database ID. |
| `description` | string | Database description. |
| `formCount` | number | Number of forms. |
| `label` | string | Database label. |
| `owner` | object | Database owner. |
| `recordCount` | number | Total record count. |
| `userCount` | number | Number of invited users. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/billingAccounts/:accountId/databases` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-billing-account-databases.md) for the provider-specific parameters and requirements.

