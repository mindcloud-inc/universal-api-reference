# Pipedrive: Get All Product Fields

Retrieves product fields from Pipedrive.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-all-deal-fields-copy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-all-deal-fields-copy?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-all-deal-fields-copy?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldCode": "string",
      "fieldName": "Ava Chen",
      "fieldType": "string",
      "isCustomField": true,
      "isOptionalResponseField": true,
      "options": {},
      "subfields": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldCode` | string |  |
| `fieldName` | string |  |
| `fieldType` | string |  |
| `isCustomField` | boolean |  |
| `isOptionalResponseField` | boolean |  |
| `options` | object |  |
| `subfields` | object |  |

## Native endpoint

Through the native Pipedrive API, this operation is `GET v2/productFields` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-deal-fields-copy.md) for the provider-specific parameters and requirements.

