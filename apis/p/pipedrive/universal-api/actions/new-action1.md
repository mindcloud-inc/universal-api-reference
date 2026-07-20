# Pipedrive: Get All Deal Fields

Retrieves deal fields from Pipedrive.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/new-action1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/new-action1?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/new-action1?${params}`, {
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

Through the native Pipedrive API, this operation is `GET v2/dealFields` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/new-action1.md) for the provider-specific parameters and requirements.

