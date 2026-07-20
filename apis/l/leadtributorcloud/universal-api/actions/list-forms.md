# leadtributor.cloud: List Forms

Retrieves forms from leadtributor.cloud.

```
GET https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a leadtributor.cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/list-forms?${params}`, {
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
      "definition": {
        "interest": {
          "fieldOrder": [
            "string"
          ],
          "fields": {}
        },
        "prospect": {
          "fieldOrder": [
            "string"
          ],
          "fields": {}
        }
      },
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "owner": "string",
      "serial": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `definition.interest.fieldOrder` | array<string> | Interest field order. |
| `definition.interest.fields` | object | Interest field definitions for the form. |
| `definition.prospect.fieldOrder` | array<string> | Prospect field order. |
| `definition.prospect.fields` | object | Prospect field definitions for the form. |
| `description` | string | Form description. |
| `id` | string | Form ID. |
| `name` | string | Form name. |
| `owner` | string | Form owner URN. |
| `serial` | number | Form serial number. |

## Native endpoint

Through the native leadtributor.cloud API, this operation is `GET /forms` (base URL `https://api.leadtributor.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

