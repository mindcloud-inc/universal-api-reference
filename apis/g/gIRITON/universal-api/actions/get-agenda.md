# GIRITON: Get Agenda

Retrieves a specific agenda from GIRITON.

```
GET https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-agenda
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-agenda?connectionId=$CONNECTION_ID&agendaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agendaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/get-agenda?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "entryTimestamp": "2026-05-07T12:00:00.000Z",
      "fields": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entryTimestamp` | date | Agenda entry timestamp. |
| `fields` | array<object> | Agenda field definitions. |
| `id` | string | Agenda ID. |
| `name` | string | Agenda name. |

## Native endpoint

Through the native GIRITON API, this operation is `GET /agendas/:agendaId` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agenda.md) for the provider-specific parameters and requirements.

