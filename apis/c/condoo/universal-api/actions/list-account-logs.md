# condoo: List Account Logs

Retrieves account logs from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-account-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-account-logs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-account-logs?${params}`, {
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
| `continentCode` | string | no | Optional continent code selector. |
| `countryCode` | string | no | Optional country code selector. |
| `deviceType` | string | no | Optional device type selector. |
| `search` | string | no | Optional search string. |
| `searchBy` | string | no | Optional search field. Allowed value: city_name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city_name": "Ava Chen",
      "continent_code": "string",
      "country_code": "string",
      "datetime": "2026-05-07T12:00:00.000Z",
      "device_type": "string",
      "ip": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city_name` | string |  |
| `continent_code` | string |  |
| `country_code` | string |  |
| `datetime` | date |  |
| `device_type` | string |  |
| `ip` | string |  |
| `type` | string |  |

## Native endpoint

Through the native condoo API, this operation is `GET /logs/` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-account-logs.md) for the provider-specific parameters and requirements.

