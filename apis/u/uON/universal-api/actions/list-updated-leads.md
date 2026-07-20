# U-ON: List Updated Leads

Retrieves leads updated in U-ON within a date range.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-updated-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-updated-leads?connectionId=$CONNECTION_ID&date_from=2026-05-07T12%3A00%3A00.000Z&date_to=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date_from": "2026-05-07T12:00:00.000Z",
  "date_to": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-updated-leads?${params}`, {
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
| `date_from` | date | yes | date_from path parameter |
| `date_to` | date | yes | date_to path parameter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_email": "ava@example.com",
      "client_id": 1,
      "client_name": "Ava Chen",
      "client_phone": "string",
      "client_sname": "Ava Chen",
      "client_surname": "Ava Chen",
      "dat": "2026-05-07T12:00:00.000Z",
      "dat_updated": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "id_internal": "string",
      "id_system": "string",
      "manager_id": 1,
      "manager_name": "Ava Chen",
      "manager_sname": "Ava Chen",
      "manager_surname": "Ava Chen",
      "notes": "string",
      "source": "string",
      "source_id": 1,
      "status": "string",
      "status_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_email` | string | E-mail клиента / E-mail client |
| `client_id` | number | ID клиента / Client ID |
| `client_name` | string | Имя клиента / The name of the customer |
| `client_phone` | string | Телефон клиента / Phone customer |
| `client_sname` | string | Отчество клиента / First name of client |
| `client_surname` | string | Фамилия клиента / The name of the client |
| `dat` | date | Дата создания заявки / Creation date of the application |
| `dat_updated` | date | Дата последнего обновления заявки / Date of last update of the application |
| `id` | string | ID / ID |
| `id_internal` | string | Внутренний номер / Internal number |
| `id_system` | string | Системный ID / System ID |
| `manager_id` | number | ID менеджера / ID Manager |
| `manager_name` | string | Имя менеджера / The name of the Manager |
| `manager_sname` | string | Отчество менеджера / The patronymic of the Manager |
| `manager_surname` | string | Фамилия менеджера / The name of the Manager |
| `notes` | string | Примечание / Note |
| `source` | string | Наименование источника / Source name |
| `source_id` | number | ID источника / Source ID |
| `status` | string | Наименование статуса / Name status |
| `status_id` | number | ID статуса / ID status |

## Native endpoint

Through the native U-ON API, this operation is `GET /leads/updated/{date_from}/{date_to}/{page}.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-updated-leads.md) for the provider-specific parameters and requirements.

