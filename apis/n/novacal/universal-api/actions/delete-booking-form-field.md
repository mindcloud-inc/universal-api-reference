# Novacal: Delete Booking Form Field

Deletes an existing booking form field from Novacal.

```
DELETE https://connect.mindcloud.co/v1/universal/novacal/latest/actions/delete-booking-form-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novacal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/novacal/latest/actions/delete-booking-form-field?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novacal/latest/actions/delete-booking-form-field?${params}`, {
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
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Delete status message. |
| `success` | boolean | Whether the delete request succeeded. |

## Native endpoint

Through the native Novacal API, this operation is `DELETE /v1/event-types/:eventType/booking-forms/:field` (base URL `https://api.novacal.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-booking-form-field.md) for the provider-specific parameters and requirements.

