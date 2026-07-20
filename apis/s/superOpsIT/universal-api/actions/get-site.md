# SuperOps IT: Get Site



```
GET https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-site?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-site?${params}`, {
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
| `id` | string | yes | The ID of the site to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "getSite": {
        "address": {
          "addressId": "string",
          "countryCode": "string"
        },
        "contactNumber": "string",
        "id": "string",
        "name": "Ava Chen",
        "timezoneCode": "string",
        "working24x7": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `getSite.address.addressId` | string |  |
| `getSite.address.countryCode` | string |  |
| `getSite.contactNumber` | string |  |
| `getSite.id` | string |  |
| `getSite.name` | string |  |
| `getSite.timezoneCode` | string |  |
| `getSite.working24x7` | boolean |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

