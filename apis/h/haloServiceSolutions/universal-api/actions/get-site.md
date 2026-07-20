# Halo Service Solutions: Get Site

Retrieves a site from Halo Service Solutions.

```
GET https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-site?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-site?${params}`, {
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
| `id` | number | yes | Site ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_id": 1,
      "client_name": "Ava Chen",
      "clientsite_name": "Ava Chen",
      "datecreated": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "inactive": true,
      "isinvoicesite": true,
      "maincontact_id": 1,
      "name": "Ava Chen",
      "sla_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_id` | number |  |
| `client_name` | string |  |
| `clientsite_name` | string |  |
| `datecreated` | date |  |
| `id` | number |  |
| `inactive` | boolean |  |
| `isinvoicesite` | boolean |  |
| `maincontact_id` | number |  |
| `name` | string |  |
| `sla_id` | number |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `GET /Site/:id` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

