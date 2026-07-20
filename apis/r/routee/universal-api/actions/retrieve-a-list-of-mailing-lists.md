# Routee: Retrieve a list of mailing lists

Retrieves a list of mailing lists from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-a-list-of-mailing-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-a-list-of-mailing-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-a-list-of-mailing-lists?${params}`, {
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
| `limit` | number | no | the number of records |
| `offset` | string | no | offset (first record to be displayed) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active_email_qty": "ava@example.com",
      "all_email_qty": "ava@example.com",
      "creationdate": "string",
      "id": "string",
      "inactive_email_qty": "ava@example.com",
      "name": "Ava Chen",
      "status": "string",
      "status_explain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_email_qty` | string |  |
| `all_email_qty` | string |  |
| `creationdate` | string |  |
| `id` | string |  |
| `inactive_email_qty` | string |  |
| `name` | string |  |
| `status` | string |  |
| `status_explain` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /addressbooks` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-a-list-of-mailing-lists.md) for the provider-specific parameters and requirements.

