# Dotdigital: Get All Custom Identifiers

Retrieves custom identifiers defined in Dotdigital.

```
GET https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-all-custom-identifiers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotdigital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-all-custom-identifiers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-all-custom-identifiers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dotdigital API returns.

## Native endpoint

Through the native Dotdigital API, this operation is `GET /configuration/v3/customIdentifiers` (base URL `https://r2-api.dotmailer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-custom-identifiers.md) for the provider-specific parameters and requirements.

