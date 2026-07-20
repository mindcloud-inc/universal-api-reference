# eTermin: Delete Appointment

Deletes an existing appointment from eTermin.

```
DELETE https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/delete-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/delete-appointment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/delete-appointment?${params}`, {
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
| `appid` | number | no | AppID of the appointment (relates to the ID) |
| `id` | string | no | ID of the appointment, <b>use externalid instead, if you use the parameter sync=1 or sendemail=1</b> (relates to the ExternalID) |
| `start` | string | no | Start date of the appointments. |
| `end` | string | no | End date of the appointments. |
| `sync` | boolean | no | True if the appointment should be synchronized with external calendars (use externalid instead of id Parameter) |
| `sendemail` | boolean | no | True if an email should be sent to the customer (use externalid instead of id Parameter) |
| `msgtype` | number | no | Defines which template should be sent |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eTermin API returns.

## Native endpoint

Through the native eTermin API, this operation is `DELETE /api/appointment` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-appointment.md) for the provider-specific parameters and requirements.

