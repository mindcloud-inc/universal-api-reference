# Bulldog-WP: List campaign contacts

Retrieves campaign contacts from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-campaign-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-campaign-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-campaign-contacts?${params}`, {
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
| `campaignId` | string | yes | Campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ack": "string",
      "campaign": {},
      "date": "2026-05-07T12:00:00.000Z",
      "group": "string",
      "id": "string",
      "kind": "string",
      "name": "Ava Chen",
      "phone": "string",
      "status": "string",
      "wabaId": "string",
      "wabaWid": "string",
      "wid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ack` | string |  |
| `campaign` | object |  |
| `date` | date |  |
| `group` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `status` | string |  |
| `wabaId` | string |  |
| `wabaWid` | string |  |
| `wid` | string |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /campaigns/{campaignId}/contacts` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-campaign-contacts.md) for the provider-specific parameters and requirements.

