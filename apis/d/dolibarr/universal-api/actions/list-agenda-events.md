# Dolibarr: List Agenda Events

Retrieves a list of agenda events from Dolibarr.

```
GET https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/list-agenda-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dolibarr `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/list-agenda-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/list-agenda-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "authorid": "string",
      "datec": 1,
      "datef": 1,
      "datep": 1,
      "elementid": "string",
      "elementtype": "string",
      "id": "string",
      "label": "string",
      "ref": "string",
      "status": "string",
      "type": "string",
      "type_code": "string",
      "type_label": "string",
      "userownerid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorid` | string | Author user id. |
| `datec` | number | Creation timestamp. |
| `datef` | number | Event end timestamp. |
| `datep` | number | Event start timestamp. |
| `elementid` | string | Linked element id. |
| `elementtype` | string | Linked element type. |
| `id` | string | Dolibarr agenda event id. |
| `label` | string | Event label. |
| `ref` | string | Agenda event reference. |
| `status` | string | Event status. |
| `type` | string | Event type key. |
| `type_code` | string | Event type code. |
| `type_label` | string | Event type label. |
| `userownerid` | string | Owner user id. |

## Native endpoint

Through the native Dolibarr API, this operation is `GET /agendaevents` (base URL `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-agenda-events.md) for the provider-specific parameters and requirements.

