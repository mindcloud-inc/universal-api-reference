# PBX Yeastar: Get Menu Options

Retrieves menu options from PBX Yeastar.

```
GET https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/get-menu-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PBX Yeastar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/get-menu-options?connectionId=$CONNECTION_ID&menu=extension" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "menu": "extension"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/get-menu-options?${params}`, {
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
| `menu` | string | yes | Yeastar menu option category to query, such as extension, org_list, trunk, phonebook, queue, or conference. Example: `extension`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "errcode": 1,
      "errmsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Menu option records. |
| `errcode` | number | Yeastar result code. 0 means success. |
| `errmsg` | string | Yeastar result message. |

## Native endpoint

Through the native PBX Yeastar API, this operation is `GET /system/get_menuoptions` (base URL `{{credentials.baseUrl}}/openapi/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-menu-options.md) for the provider-specific parameters and requirements.

