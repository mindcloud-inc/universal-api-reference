# UKG Pro: Get Platform Configuration Fields



```
GET https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-platform-configuration-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UKG Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-platform-configuration-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-platform-configuration-fields?${params}`, {
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
| `className` | string | no | Default: `Employee`. |
| `fields` | string | no | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "className": "Ava Chen",
      "fieldRows": [
        {
          "fieldName": "Ava Chen",
          "fieldValue": "string"
        }
      ],
      "keyName": "Ava Chen",
      "keyValue": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `className` | string |  |
| `fieldRows[].fieldName` | string |  |
| `fieldRows[].fieldValue` | string |  |
| `keyName` | string |  |
| `keyValue` | string |  |

## Native endpoint

Through the native UKG Pro API, this operation is `GET personnel/v1/platform-configuration-fields/class-name/:className` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-platform-configuration-fields.md) for the provider-specific parameters and requirements.

