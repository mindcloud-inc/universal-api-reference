# IN-D KYC India: Get Connector Documentation

Retrieves the IN-D KYC India connector documentation.

```
GET https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/get-connector-documentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IN-D KYC India `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/get-connector-documentation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/get-connector-documentation?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IN-D KYC India API returns.

## Native endpoint

Through the native IN-D KYC India API, this operation is `GET https://learn.microsoft.com/en-us/connectors/indkycindia/` (base URL `https://api.kyc.in-d.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connector-documentation.md) for the provider-specific parameters and requirements.

