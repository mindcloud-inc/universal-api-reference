# Audome: Get Client Project



```
GET https://connect.mindcloud.co/v1/universal/audome/latest/actions/get-client-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Audome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/audome/latest/actions/get-client-project?connectionId=$CONNECTION_ID&uuid=ee18cc30-2f6f-11f1-a641-dbdcc39885eb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "ee18cc30-2f6f-11f1-a641-dbdcc39885eb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/audome/latest/actions/get-client-project?${params}`, {
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
| `uuid` | string | yes | UUID of the client project to fetch. Example: `ee18cc30-2f6f-11f1-a641-dbdcc39885eb`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Audome API returns.

## Native endpoint

Through the native Audome API, this operation is `GET /client-projects/:uuid` (base URL `https://app.audome.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client-project.md) for the provider-specific parameters and requirements.

