# easybill: Get Serial Number

Retrieves a serial number from easybill by ID.

```
GET https://connect.mindcloud.co/v1/universal/easybill/latest/actions/get-serial-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a easybill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easybill/latest/actions/get-serial-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easybill/latest/actions/get-serial-number?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native easybill API returns.

## Native endpoint

Through the native easybill API, this operation is `GET /serial-numbers/{id}` (base URL `https://api.easybill.de/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-serial-number.md) for the provider-specific parameters and requirements.

