# Rachio Smart Lighting Controller: List Lighting Areas



```
GET https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/list-lighting-areas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Lighting Controller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/list-lighting-areas?connectionId=$CONNECTION_ID&userId=6c9ef499-10e7-40e4-9986-27aeb82a6d77" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "6c9ef499-10e7-40e4-9986-27aeb82a6d77"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/list-lighting-areas?${params}`, {
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
| `userId` | string | yes | The person ID returned by Get Current Person ID. Example: `6c9ef499-10e7-40e4-9986-27aeb82a6d77`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rachio Smart Lighting Controller API returns.

## Native endpoint

Through the native Rachio Smart Lighting Controller API, this operation is `GET https://cloud-rest.rach.io/lighting/listLightingAreas/:userId` (base URL `https://cloud-rest.rach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lighting-areas.md) for the provider-specific parameters and requirements.

