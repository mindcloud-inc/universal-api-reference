# Google Ads: Get User List

Retrieves a user list from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/get-user-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/get-user-list?connectionId=$CONNECTION_ID&customerId=1234567890&userListId=1111111111&query=SELECT%20user_list.id%2C%20user_list.name%2C%20user_list.resource_name%20FROM%20user_list%20WHERE%20user_list.id%20%3D%201234567890%20LIMIT%201" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "userListId": "1111111111",
  "query": "SELECT user_list.id, user_list.name, user_list.resource_name FROM user_list WHERE user_list.id = 1234567890 LIMIT 1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/get-user-list?${params}`, {
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
| `customerId` | list | yes | Customer ID that owns the Google Ads resources (without dashes). Example: `1234567890`. |
| `userListId` | string | yes | User list ID to retrieve. Example: `1111111111`. |
| `query` | string | yes | GAQL query to fetch the target user list. Example: `SELECT user_list.id, user_list.name, user_list.resource_name FROM user_list WHERE user_list.id = 1234567890 LIMIT 1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "userList": {
        "id": "string",
        "name": "Ava Chen",
        "resourceName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `userList.id` | string |  |
| `userList.name` | string |  |
| `userList.resourceName` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-list.md) for the provider-specific parameters and requirements.

