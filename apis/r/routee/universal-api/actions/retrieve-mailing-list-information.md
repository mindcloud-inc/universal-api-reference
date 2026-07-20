# Routee: Retrieve mailing list information

Retrieves mailing list information from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-mailing-list-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-mailing-list-information?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-mailing-list-information?${params}`, {
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
| `id` | string | yes | List ID |

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

Through the native Routee API, this operation is `GET /addressbooks/:id` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-mailing-list-information.md) for the provider-specific parameters and requirements.

