# Ortto: List Person Custom Fields



```
GET https://connect.mindcloud.co/v1/universal/ortto/latest/actions/list-person-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/list-person-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ortto/latest/actions/list-person-custom-fields?${params}`, {
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
      "fields": [
        {
          "field": {
            "displayType": "string",
            "id": "string",
            "liquidName": "Ava Chen",
            "name": "Ava Chen"
          },
          "trackedValue": true
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields[].field.displayType` | string |  |
| `fields[].field.id` | string |  |
| `fields[].field.liquidName` | string |  |
| `fields[].field.name` | string |  |
| `fields[].trackedValue` | boolean |  |

## Native endpoint

Through the native Ortto API, this operation is `POST /person/custom-field/get` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-person-custom-fields.md) for the provider-specific parameters and requirements.

