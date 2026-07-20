# SuperOps IT: Create Site



```
POST https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "working24x7": true,
  "timezoneCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "working24x7": true,
    "timezoneCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The site name. |
| `working24x7` | boolean | yes | Whether the site works 24x7. |
| `timezoneCode` | string | yes | The IANA timezone code for the site. |
| `contactNumber` | string | no | The site contact number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createSite": {
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
| `createSite.address.addressId` | string |  |
| `createSite.address.countryCode` | string |  |
| `createSite.contactNumber` | string |  |
| `createSite.id` | string |  |
| `createSite.name` | string |  |
| `createSite.timezoneCode` | string |  |
| `createSite.working24x7` | boolean |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site.md) for the provider-specific parameters and requirements.

