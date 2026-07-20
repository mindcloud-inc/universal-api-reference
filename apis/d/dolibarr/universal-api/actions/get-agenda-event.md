# Dolibarr: Get Agenda Event

Retrieves an agenda event from Dolibarr.

```
GET https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-agenda-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dolibarr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-agenda-event?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-agenda-event?${params}`, {
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
| `id` | number | yes | Dolibarr agenda event ID. |

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

Through the native Dolibarr API, this operation is `GET /agendaevents/{id}` (base URL `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agenda-event.md) for the provider-specific parameters and requirements.

