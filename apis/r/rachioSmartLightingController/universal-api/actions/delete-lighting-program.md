# Rachio Smart Lighting Controller: Delete Lighting Program



```
DELETE https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/delete-lighting-program
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Lighting Controller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/delete-lighting-program?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/delete-lighting-program?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rachio Smart Lighting Controller API returns.

## Native endpoint

Through the native Rachio Smart Lighting Controller API, this operation is `DELETE https://cloud-rest.rach.io/lighting/deleteLightingProgram/:id` (base URL `https://cloud-rest.rach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-lighting-program.md) for the provider-specific parameters and requirements.

