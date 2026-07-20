# Abyssale: Get Design Format Details

Retrieves design format details from Abyssale.

```
GET https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/get-design-format-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abyssale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/get-design-format-details?connectionId=$CONNECTION_ID&designId=64238d01-d402-474b-8c2d-fbc957e9d290&formatSpecifier=facebook-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "designId": "64238d01-d402-474b-8c2d-fbc957e9d290",
  "formatSpecifier": "facebook-post"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/get-design-format-details?${params}`, {
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
| `designId` | string | yes | Unique identifier of the design Example: `64238d01-d402-474b-8c2d-fbc957e9d290`. |
| `formatSpecifier` | string | yes | Format name or UID Example: `facebook-post`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Abyssale API returns.

## Native endpoint

Through the native Abyssale API, this operation is `GET /designs/:designId/formats/:formatSpecifier` (base URL `https://api.abyssale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-design-format-details.md) for the provider-specific parameters and requirements.

