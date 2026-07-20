# Rubitime: Get Schedule

Retrieves booking dates and times from Rubitime.

```
GET https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/get-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rubitime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/get-schedule?connectionId=$CONNECTION_ID&branchId=1&cooperatorId=1&serviceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "branchId": "1",
  "cooperatorId": "1",
  "serviceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/get-schedule?${params}`, {
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
| `branchId` | number | yes | Rubitime branch ID. |
| `cooperatorId` | number | yes | Rubitime employee/cooperator ID. |
| `serviceId` | number | yes | Rubitime service ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `onlyAvailable` | number | no | Use 1 to return only available slots or 0 to return only occupied slots. Omit to return all slots. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rubitime API returns.

## Native endpoint

Through the native Rubitime API, this operation is `POST /get-schedule` (base URL `https://rubitime.ru/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule.md) for the provider-specific parameters and requirements.

