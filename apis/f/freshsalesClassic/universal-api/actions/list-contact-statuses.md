# Freshsales Classic: List Contact Statuses

Retrieves contact statuses from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-contact-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-contact-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-contact-statuses?${params}`, {
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
      "forecastType": "string",
      "id": 1,
      "lifecycleStageId": 1,
      "name": "Ava Chen",
      "partial": true,
      "position": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `forecastType` | string | Forecast classification. |
| `id` | number | Contact status ID. |
| `lifecycleStageId` | number | Related lifecycle stage ID. |
| `name` | string | Contact status name. |
| `partial` | boolean | Whether the status is partial. |
| `position` | number | Status position. |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /selector/contact_statuses` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-statuses.md) for the provider-specific parameters and requirements.

