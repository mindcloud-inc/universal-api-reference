# SmartReach: List Do Not Contact List

Retrieves do not contact entries from SmartReach.

```
GET https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-do-not-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-do-not-contact-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-do-not-contact-list?${params}`, {
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
| `olderThan` | number | no | timestamp in unix epoch milliseconds |
| `newerThan` | number | no | timestamp in unix epoch milliseconds |

## Response

```json
{
  "success": true,
  "data": [
    {
      "do_not_contacts": [
        {
          "do_not_contact_type": "string",
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "links": {
        "next": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `do_not_contacts[].do_not_contact_type` | string |  |
| `do_not_contacts[].id` | string |  |
| `do_not_contacts[].name` | string |  |
| `links.next` | string |  |

## Native endpoint

Through the native SmartReach API, this operation is `GET /do_not_contact` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-do-not-contact-list.md) for the provider-specific parameters and requirements.

