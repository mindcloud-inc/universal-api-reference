# Restoplace: List Available Times

Retrieves available booking times from Restoplace.

```
GET https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/list-available-times
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restoplace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/list-available-times?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/list-available-times?${params}`, {
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
| `date` | string | no | Date to search for available times in YYYY-MM-DD format. |
| `length` | number | no | Reservation length in minutes. |
| `floorId` | number | no | Hall ID to search within. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shift` | string | no | Optional shift selector supported by the provider. |
| `dateFormat` | string | no | Optional provider date format override. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restoplace API returns.

## Native endpoint

Through the native Restoplace API, this operation is `GET /times/` (base URL `https://api.restoplace.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-times.md) for the provider-specific parameters and requirements.

