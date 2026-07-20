# Crexendo: List User SMS Numbers

Retrieves SMS numbers for a user in Crexendo.

```
GET https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-user-sms-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crexendo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-user-sms-numbers?connectionId=$CONNECTION_ID&limit=25&offset=0&domain=string&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "domain": "string",
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-user-sms-numbers?${params}`, {
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
| `domain` | string | yes | Domain identifier, for example apps.mindcloud.co. |
| `user` | string | yes | User extension or identifier, for example 1000. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "application": "string",
      "carrier": "string",
      "dest": "string",
      "domain": "string",
      "group-mms-capable": true,
      "mms-capable": true,
      "number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application` | string |  |
| `carrier` | string |  |
| `dest` | string |  |
| `domain` | string |  |
| `group-mms-capable` | boolean |  |
| `mms-capable` | boolean |  |
| `number` | string |  |

## Native endpoint

Through the native Crexendo API, this operation is `GET /domains/:domain/users/:user/smsnumbers` (base URL `https://ns-api.com/ns-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-sms-numbers.md) for the provider-specific parameters and requirements.

