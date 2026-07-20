# Temp Stick: Get Email Reports

Retrieves Temp Stick email report settings and downloadable reports.

```
GET https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-email-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temp Stick `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-email-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-email-reports?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Temp Stick API returns.

## Native endpoint

Through the native Temp Stick API, this operation is `GET /user/email-reports` (base URL `https://tempstickapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-reports.md) for the provider-specific parameters and requirements.

