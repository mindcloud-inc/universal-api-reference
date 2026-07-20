# LabsMobile: List OTP Environments

Retrieves OTP environments from LabsMobile.

```
GET https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/list-otp-environments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LabsMobile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/list-otp-environments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/list-otp-environments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LabsMobile API returns.

## Native endpoint

Through the native LabsMobile API, this operation is `GET /otp/getEnvList` (base URL `https://api.labsmobile.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-otp-environments.md) for the provider-specific parameters and requirements.

