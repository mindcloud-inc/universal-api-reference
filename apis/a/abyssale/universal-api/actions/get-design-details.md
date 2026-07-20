# Abyssale: Get Design Details

Retrieves design details from Abyssale.

```
GET https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/get-design-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abyssale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/get-design-details?connectionId=$CONNECTION_ID&designId=7dc0229b-cc0e-4fe5-971d-325164480887" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "designId": "7dc0229b-cc0e-4fe5-971d-325164480887"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/get-design-details?${params}`, {
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
| `designId` | string | yes | Unique identifier (UUID) of the design Example: `7dc0229b-cc0e-4fe5-971d-325164480887`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Abyssale API returns.

## Native endpoint

Through the native Abyssale API, this operation is `GET /designs/:designId` (base URL `https://api.abyssale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-design-details.md) for the provider-specific parameters and requirements.

