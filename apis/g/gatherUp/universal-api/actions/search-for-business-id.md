# GatherUp: Search for Business ID

Finds a business ID in GatherUp.

```
GET https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/search-for-business-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/search-for-business-id?connectionId=$CONNECTION_ID&by=string&search=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "by": "string",
  "search": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/search-for-business-id?${params}`, {
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
| `by` | string | yes | Search by... Possible values: customField , extraField |
| `search` | string | yes | Search value |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": 1,
      "errorCode": 1,
      "errorMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | number |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /business/search` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-for-business-id.md) for the provider-specific parameters and requirements.

