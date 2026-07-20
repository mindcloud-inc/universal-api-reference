# Cituro Universal API Examples

These examples use the MindCloud API key and Cituro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Appointment

Retrieves an appointment record from Cituro.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cituro/latest/actions/get-appointment?connectionId=$CONNECTION_ID&appointmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appointmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cituro/latest/actions/get-appointment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Appointment action reference](actions/get-appointment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cituro/latest/actions/get-appointment).
