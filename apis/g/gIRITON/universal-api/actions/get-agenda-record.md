# GIRITON: Get Agenda Record

Retrieves a specific record from a GIRITON agenda.

```
GET https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-agenda-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-agenda-record?connectionId=$CONNECTION_ID&agendaId=string&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agendaId": "string",
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-agenda-record?${params}`, {
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
| `agendaId` | string | yes | Agenda ID. |
| `recordId` | string | yes | Agenda record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFieldId1": "string",
      "customFieldId2": 1,
      "customFieldId3": true,
      "entryTimestamp": "2026-05-07T12:00:00.000Z",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFieldId1` | string | Custom field value. |
| `customFieldId2` | number | Custom field value. |
| `customFieldId3` | boolean | Custom field value. |
| `entryTimestamp` | date | Agenda record entry timestamp. |
| `id` | string | Agenda record ID. |

## Native endpoint

Through the native GIRITON API, this operation is `GET /agendas/:agendaId/records/:recordId` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agenda-record.md) for the provider-specific parameters and requirements.

