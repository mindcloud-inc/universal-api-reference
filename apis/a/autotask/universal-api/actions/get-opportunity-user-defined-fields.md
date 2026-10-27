# Autotask: Get Opportunity User-Defined Fields



```
GET https://connect.mindcloud.co/v1/universal/autotask/latest/actions/get-opportunity-user-defined-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autotask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autotask/latest/actions/get-opportunity-user-defined-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autotask/latest/actions/get-opportunity-user-defined-fields?${params}`, {
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
      "defaultValue": "string",
      "description": "string",
      "isPickList": true,
      "isQueryable": true,
      "isReadOnly": true,
      "isReference": true,
      "isRequired": true,
      "isSupportedWebhookField": true,
      "label": "string",
      "length": 1,
      "name": "Ava Chen",
      "picklistParentValueField": "string",
      "picklistValues": [
        {}
      ],
      "referenceEntityType": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultValue` | string | Default value of the user-defined field. |
| `description` | string | Description of the user-defined field. |
| `isPickList` | boolean | Whether the user-defined field is a pick list. |
| `isQueryable` | boolean | Whether the user-defined field can be used in queries. |
| `isReadOnly` | boolean | Whether the user-defined field is read-only. |
| `isReference` | boolean | Whether the user-defined field references another entity. |
| `isRequired` | boolean | Whether the user-defined field is required. |
| `isSupportedWebhookField` | boolean | Whether the user-defined field is supported by Autotask webhooks. |
| `label` | string | Display label of the user-defined field. |
| `length` | number | Maximum length of the user-defined field value. |
| `name` | string | Internal name of the user-defined field. |
| `picklistParentValueField` | string | Parent value field for dependent pick lists. |
| `picklistValues` | array<object> | Allowed pick list values for the user-defined field. |
| `referenceEntityType` | string | Entity type referenced when the field is a reference field. |
| `type` | string | Autotask data type of the user-defined field. |

## Native endpoint

Through the native Autotask API, this operation is `GET /Opportunities/entityInformation/userDefinedFields` (base URL `https://webservices14.autotask.net/ATServicesRest/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-opportunity-user-defined-fields.md) for the provider-specific parameters and requirements.

