# RD Station Marketing: List Custom Fields



```
GET https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-custom-fields?${params}`, {
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
          "apiIdentifier": "string",
          "customField": true,
          "dataType": "string",
          "label": {
            "default": "string"
          },
          "name": {
            "default": "Ava Chen"
          },
          "presentationType": "string",
          "uuid": "string",
          "validationRules": {
            "validOptions": [
              {
                "value": "string"
              }
            ]
          }
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
| `fields[].apiIdentifier` | string |  |
| `fields[].customField` | boolean |  |
| `fields[].dataType` | string |  |
| `fields[].label.default` | string |  |
| `fields[].name.default` | string |  |
| `fields[].presentationType` | string |  |
| `fields[].uuid` | string |  |
| `fields[].validationRules.validOptions[].value` | string |  |

## Native endpoint

Through the native RD Station Marketing API, this operation is `GET /platform/contacts/fields` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-fields.md) for the provider-specific parameters and requirements.

